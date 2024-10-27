## Assignment 1: Guess the Number Game

Create a small game where the program chooses a random number between 1 and 10, and the user has to guess it.

1. Import the `random` module.
2. Use `random.randint(1, 10)` to generate a random number.
3. Use a `while` loop to keep asking the user for their guess until they guess correctly.
4. After each incorrect guess, print a hint if the guess was too high or too low.
5. When the user guesses correctly, print a congratulatory message and exit the loop.

### Example Output

```plaintext
Guess the number (between 1 and 10): 3
Too low! Try again.
Guess the number (between 1 and 10): 7
Congratulations! You've guessed the number!
```
