# WordWhiz

A C# console application designed to help solve the [Wordle game](https://www.nytimes.com/games/wordle/index.html) by filtering a list of valid words and using different strategies to make optimal guesses.

## Features

- **Strategy Pattern**: The bot utilizes a flexible architecture allowing multiple guessing strategies to be implemented and tested.
- **Word Filtering**: After each guess, the bot filters the word list based on feedback from the game (correct, present, and absent letters).
- **Customizable Strategies**: Easily implement new strategies for guessing, such as random guesses, frequency analysis etc.
