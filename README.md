# WordWhiz

A C# console application designed to help solve the [Wordle game](https://www.nytimes.com/games/wordle/index.html) by filtering a list of valid words and using different strategies to suggest optimal guesses.

## Features

- **Strategy Pattern**: The bot leverages the strategy pattern, allowing multiple guessing strategies to be implemented and tested; allowing flexibility in how the bot selects guesses.
- **Interactive Word Filtering**: After each guess, the bot dynamically filters the word list based on user input, narrowing down possible answers.
  
## Strategies Included

1. **Pattern Matching Strategy**: 
    - Filters words based on the current pattern, required letters, excluded letters, and an exclude pattern.
    - Suggests the next possible guess by grouping remaining words based on common letters at unknown positions.
  
## How It Works

1. **Load Word List**: The bot starts by loading a list of valid 5-letter words from a text file.
2. **Make a Guess**: Using the initial filtering criteria, the bot suggests possible guesses.
3. **Receive Feedback**: After making a guess in the Wordle game, you input the feedback into the bot in the format:
   [Pattern]:[RequiredLetters]:[Excludes]:[ExcludePattern] (e.g. +a++s:[g][p]----p)
   - Pattern (`+` for unknown letters, known letters in their correct positions),
   - Required letters (letters in the word, but not yet placed),
   - Excludes (letters not in the word),
   - Exclude Pattern (letters in the wrong position, represented by `-`).
   The input should be in lower case letters. 
5. **Filter Words**: Based on this feedback, the word list is filtered to remove invalid words.
6. **Suggestions**: The bot groups possible words based on common letters at unknown positions and suggests the next guess.
7. **Repeat**: The process continues until the word is solved.
