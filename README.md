# wordle-kata

Wordle game implementation kata.

## Description

Wordle is a popular internet game where the goal is to guess a randomly selected 5-letter word within a limited number of attempts.

As one cannot find the expected word by luck, the player is provided a feedback after each attempt to help him guess the solution.

The feedback is provided as a series of tiles (there are as many tiles as letters in the word to be guessed).

The tile is :

- 🟩 (green) if the proposed letter is in the word at the same location,
- 🟨 (yellow) if the letter is in the word but at another location,
- ⬛ (grey) if the letter is not present in the word.

## Example of game

Let's imagine that the word to be guessed is CRAFT.

First attempt is : FLIRT

Feedback is : 🟨⬛⬛🟨🟩


Second attempt is : DRIFT

Feedback is : ⬛🟩⬛🟩🟩


Third attempt is : DRAFT

Feedback is : ⬛🟩🟩🟩🟩


Fourth (and winning) attempt is : CRAFT

Feedback is : 🟩🟩🟩🟩🟩

## Running the kata

### Provide the feedback

The first feature that you can develop is as follows : given a solution word, and an attempt word, provide feedback as in the examples.

### Handle a game

With the second feature, you have to manage a full game and in order to do so, keep track of all the attempts in the game.
After each attempt, you are able to provide an history of the feedbacks for the game, as follows :

🟨⬛⬛🟨🟩  
⬛🟩⬛🟩🟩   
⬛🟩🟩🟩🟩  
🟩🟩🟩🟩🟩

Variations of the kata :

- you may in a first iteration provide the history of the attempts as input : thus you can recompute and aggregate all the feedbacks on the fly
- in a second iteration you can try to handle the state of the game in order to remember the previous attempts

### Manage a dictionary

You need to define and manage a dictionary that contains all the accepted words.  
When a game is started, a word to be guessed is selected at random.

As an additional feature, you can check that only attempts with words present in the dictionary are valid.

### Expand the size of the words

Modify the code to accept 6-letter words, then 7-letter words and so on ...

### Change the nature of the game

Let's imagine that you must transform the Wordle game into a Super Mastermind game. Is your code enough evolutive to allow that ?