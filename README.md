# Hog
The Game of Hog is a Simulator for a Dice Game which I built as a part of CS61A's curriculum. Building it required the knowledge of control statements and higher-order functions. The starter files were provided and I only had to make changes in the hog.py file. The game has no User Interface and hence can only be played in the Terminal.

## Rules

In Hog, two players alternate turns trying to be the first to end a turn with at least GOAL total points, where GOAL defaults to 100. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes.

**Sow Sad**: If any of the dice outcomes is a 1, the current player's score for the turn is 1. For example, if a player rolls 5 dices and gets 1 in any of those, they score only 1 point for the turn.

**Pig Tail**: A player who chooses to roll zero dice scores 2 * abs(tens - ones) + 1 points; where tens, ones are the tens and ones digits of the opponent's score. The ones digit refers to the rightmost digit and the tens digit refers to the second-rightmost digit. For example, if the opponent has 69 points and the player chooses to roll zero dice, they get 2 * abs(6 - 9) + 1 = 7 points.

**Square Swine**: After a player gains points for their turn, if the resulting score is a perfect square, then increase their score to the next higher perfect square. A perfect square is any integer n where n = d * d for some integer d. For example, if a player only gets a single point from 80 and lands at 81 (which is 9 squared), then their new score becomes 100 (which is 10 squared) and they win the game.

## How to Play

```
python hog_ui.py
```
Running this in the terminal begins the game between 2 computers that both follow the always_roll_5 strategy. This strategy can be edited in the UI file to be any of the other implemented strategies.

```
python hog_ui.py -n 1
```
Running this in the terminal begins a game between a player and the computer strategy which is always_roll_5 which can be changed as mentioned.

```
python hog_ui.py -n 2
```
Running this in the terminal begins a game between 2 human players who can use any interactive strategy as they wish.
