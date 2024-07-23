
# English-Turkish Flashcard GUI

This project is a flashcard application for learning English-Turkish vocabulary. It uses Tkinter for the graphical user interface and pandas for managing the vocabulary data. The app displays flashcards with English words and their Turkish translations, allowing users to mark words as known or unknown.

## Features

- **Flashcards**: Displays English words on one side and Turkish translations on the other.
- **Vocabulary Management**: Keeps track of words that the user needs to learn.
- **Persistence**: Saves the list of words that still need to be learned to a CSV file.

## Table of Contents

- [Usage](#usage)
- [Code Overview](#code-overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)

## Usage

1. **Run the Application**:

   Execute the `main.py` script to start the application:

   ```bash
   python main.py
   ```

   The application will display a flashcard with an English word. After 3 seconds, the card will flip to show the Turkish translation. You can click the appropriate button to mark the word as known or unknown.

2. **Manage Vocabulary**:

   The application will save words that are not known to `words_to_learn.csv`. This ensures that only the words that need further study are retained.

## Code Overview

### `main.py`

This is the main script of the application, which initializes the Tkinter window and handles the flashcard functionality:

- **Imports**: Uses Tkinter for the GUI, `random` for selecting words, and `pandas` for managing vocabulary data.
- **Functions**:
  - `next_word()`: Displays the next word in the flashcard and sets a timer to flip the card.
  - `is_known()`: Marks the current word as known and updates the vocabulary CSV.
  - `flip_card()`: Flips the flashcard to show the Turkish translation.

### File Handling

- **Vocabulary Data**:
  - **`data/English_turkish.csv`**: The original file with English-Turkish word pairs.
  - **`data/words_to_learn.csv`**: Automatically generated file with words that need to be learned.

## Project Structure

- `main.py`: Main script for running the flashcard application.
- `images/`:
  - `card_front.png`: Front image of the flashcard.
  - `card_back.png`: Back image of the flashcard.
  - `wrong.png`: Button image for unknown words.
  - `right.png`: Button image for known words.
- `data/`:
  - `English_turkish.csv`: Original word pairs CSV file.
  - `words_to_learn.csv`: CSV file with words to be learned (auto-generated).

## Requirements

- **Python 3.x**
- **Pandas**: For handling CSV files.
- **Tkinter**: For the graphical user interface.

## Contributing

Contributions are welcome! If you have suggestions for improvements or bug fixes, please submit a Pull Request. Make sure to document and test your changes.

