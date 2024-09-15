
# Scrabble Word Game

This repository contains an implementation of a Scrabble-like word game in Python, where players try to form words from randomly generated hands of letters. The game also includes functionality for the computer to choose the optimal word based on a given hand.

## Features

- Random generation of a hand consisting of vowels and consonants.
- Scoring system based on Scrabble letter values.
- Ability for the player to form words from their hand and receive scores.
- Computer mode where the optimal word is chosen by the system.

## File Descriptions

### `ps4a.py`

This file contains the core logic of the word game, including:
- `loadWords()`: Loads a list of valid words from a file (`words.txt`).
- `dealHand(n)`: Generates a hand of random letters, where `n` is the number of letters.
- `getWordScore(word, n)`: Returns the score for a valid word based on Scrabble letter values.
- `playHand(hand, wordList, n)`: Allows the user to play a hand and input words to form.
- `isValidWord(word, hand, wordList)`: Checks if the word is valid given the current hand and word list.
- `playGame(wordList)`: Manages the game session, including dealing hands and keeping track of scores.

### `ps4b.py`

This file adds an additional feature where the computer selects the best possible word from a given hand:
- `compChooseWord(hand, wordList, n)`: Finds the word from the word list that gives the maximum score using the current hand.
- `compPlayHand(hand, wordList, n)`: Allows the computer to play a hand automatically by choosing the best word for each turn.

## How to Run the Game

1. Make sure you have a `words.txt` file containing a list of valid words.
2. Run the `ps4a.py` file to play the word game as a human player.
3. To let the computer play, run the `ps4b.py` file, which extends the original game with computer-playing functionality.

### Example of running the game:
\`\`\`bash
python ps4a.py  # To play as a human player
python ps4b.py  # To let the computer play
\`\`\`

## Scoring System

The score for each word is calculated using the following Scrabble letter values:

| Letter  | Value |
|---------|-------|
| A, E, I, O, U, L, N, S, T, R | 1     |
| D, G   | 2     |
| B, C, M, P | 3     |
| F, H, V, W, Y | 4     |
| K | 5     |
| J, X | 8     |
| Q, Z | 10    |

The score for a word is the sum of the points for each letter, multiplied by the length of the word, plus a 50-point bonus for using all the letters in the hand.

## Requirements

- Python 3.x
- A `words.txt` file containing a list of valid words.

## License

This project is open source and available under the MIT License.
