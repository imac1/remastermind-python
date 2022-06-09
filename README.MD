# Remastermind

## Story

Remember Mastermind, the board game with the colored pegs? Last time we walked through a solution which was fine and working, but let's face it, was not a _clean_ one.

In this project, you'll have to _refactor_ the original version. We have two goals:
- to make the code structured and readable
- to make it more general and easily parametrizable (this can be seen as a new feature).

## What are you going to learn?

- Write clean code.
- Break down the game logic into functions and reassemble them into a solid game workflow.
- Use parameters and avoid globals.
- Shorten the code using built-in methods and Pythonic expressions.

## Tasks

1. Create five top-level functions: `create_secret()`, `get_guess()`, `guess_check()`, `display_board()`, and `play_mastermind()`, and move the appropriate parts of the original code under these functions. Don't forget to remove unnecessary comments at the end.
    - There are exactly five function definitions (and no inner funtions) in the source code with the required names.
    - There are no code outside these functions, except for the import statement, global variable declarations, and the single call of `play_mastermind()`.
    - There are no unnecessary comments in the code.
    - The game play is unchanged.

2. Add parameters to the five functions so that you can remove all global variables except for `colors`.
    - There are no global variables, with the possible exception of `colors`.
    - There are no unused parameters, functions get just what they need.
    - The game play is unchanged.

3. Get rid of global variables completely. Pass the list of possible color letters to `play_mastermind(), and pass it further when needed.
    - There are no global variables, not even `colors`.
    - The game can be played with different colors (say `ABCDEF`) without any problems (and any references to the original letters `YORPGB`).
    - The game play is unchanged.

4. Get rid of references of 4, 6, 12, and call `play_mastermind` with three parameters: `colors="YORPGB"`, `code_length=4`, and `number_of_rounds=12`)
    - There are no magic literals except for the main invocation `play_mastermind(list("YORPGB"), 4, 12)`.
    - The game can be played with different color sets of different size (say `ABCDEFGH`) and different secret lengths without any problems.
    - There are no unused parameters, functions get just what they need.
    - The game play is unchanged.

5. Get rid of loops, and replace them with built-in function/method calls or comprehensions. You can keep three loops: - the one that iterates over the game rounds - the one that iterates over the invalid input attempts - the one that iterates over the history list during board display.
    - There are only three loops in the code, one each in `get_guess()`, `display_board()`, and `play_mastermind()`.

## General requirements

None

## Hints

- Use the `random.choices()` method to create the secret without loops.
- Use the `count()` and `join()` methods on strings to handle their contents more effectively.
- Use `set()` to create a collection of unique elements (i.e. a set) from another collection.
- Remember, a comment is unnecessary if it adds no significant extra information to the reader above the function and variable names along the control flow. Don't comment `# Iterate through colors` next to the line `for color in colors`.

