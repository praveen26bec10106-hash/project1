# project1



# High or Low Number Guessing Game

## About the Project

This is a simple **High or Low number guessing game** made in Python.

The idea of the game is easy: a number is shown on the screen and the player has to guess whether the next randomly generated number will be **higher or lower** than the current number.

I made this project to practice the basic Python concepts covered in class, especially functions, loops, conditions, user input, random numbers and lists.

**Project made by:** Praveen yadav  
**Under the guidance of:** Dr. Friends

---

## How the Game Works

- The game starts with a random number between **1 and 200**.
- The player starts with **50 points**.
- Before every round, the player chooses:
  - `HIGH` or `H` if they think the next number will be higher.
  - `LOW` or `L` if they think the next number will be lower.
- A new random number is then generated.
- If the guess is correct, **10 points are added**.
- If the guess is wrong, **5 points are deducted**.
- If both numbers are equal, the score does not change.
- A game can have a maximum of **10 rounds**.
- The game also stops if the player's score reaches 0.

After the game finishes, the player's final score is displayed and the result is added to the leaderboard.

---

## Main Features

### 1. Play Game
Starts a new game and asks the player for their name and guesses.

### 2. Rules
Displays the rules, scoring system, starting score and number of rounds.

### 3. Leaderboard
Stores the scores of the games played during the current run of the program and displays them in descending order.

### 4. Input Checking
The program does not accept an empty player name and keeps asking until the player enters a valid choice.

### 5. Random Number Generation
The `random` module is used to generate numbers between 1 and 200.

---

## Python Concepts Used

This project uses several basic Python concepts:

- Variables and constants
- `if`, `elif` and `else`
- `while` loops
- Functions
- User input using `input()`
- Lists
- Tuples
- Dictionary-free data handling
- Sorting using `sorted()`
- String formatting
- The `random` module
- The `main()` function
- `if __name__ == "__main__":`

---

## Functions Used

Some of the main functions in the program are:

- `get_player_name()` - takes the player's name.
- `show_rules()` - displays the game rules.
- `get_choice()` - gets and checks the HIGH/LOW choice.
- `show_leaderboard()` - displays previous scores.
- `play_game()` - contains the main game logic.
- `main()` - controls the main menu.

Keeping the program divided into functions makes the code easier to understand and modify.

---

## Scoring System

| Situation | Score Change |
|---|---:|
| Correct guess | +10 |
| Wrong guess | -5 |
| Equal numbers | 0 |
| Starting score | 50 |

The player can play for a maximum of **10 rounds**, unless the score becomes 0 earlier.

---

## Requirements

You only need:

- Python 3.x
- A terminal, command prompt, or Python IDE

No external libraries are required. The project only uses Python's built-in `random` module.

---

## How to Run

1. Make sure Python 3 is installed on your computer.
2. Save the project file as:

   `FINAL PYHON PROJECT BY PRAVEEN YADAV.py`

3. Open the folder containing the file in a terminal.
4. Run:

```bash
python "FINAL PYHON PROJECT BY PRAVEEN YADAV.py"
```

5. Select an option from the main menu.

---

## Example of the Menu

```text
HIGH OR LOW GAME
1-Play Game
2-Rules
3-Leaderboard
4-Exit
```

Choose `1` to start playing.

---

## What I Learned

While making this project, I got more practice with breaking a problem into smaller functions and using loops and conditions to control the flow of a program.

I also learned how to use the `random` module, take input from the user, update a score during a game and store multiple players' scores in a list.

The project also helped me understand how a simple Python program can be organized using a main menu and separate functions instead of putting everything in one block of code.

---

## Possible Improvements

There are a few things that could be added in a future version:

- Save the leaderboard to a file so scores are not lost when the program closes.
- Add difficulty levels.
- Add more rounds as an option.
- Improve the game interface.
- Add a high-score system.
- Add more detailed player statistics.

---

## Conclusion

The **High or Low Number Guessing Game** is a small Python project designed to apply basic programming concepts in a practical way.

It is simple to play, but it covers useful programming ideas such as functions, loops, conditions, input validation, random number generation and data storage.


