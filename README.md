# Unbeatable Tic-Tac-Toe

A Tic-Tac-Toe AI that never loses. It searches every possible future of the game with **minimax** and **alpha-beta pruning**, and always picks the best move.

## How it works

- **Minimax:** X tries to maximize the score and O tries to minimize it (+1 X wins, −1 O wins, 0 tie). The AI recursively plays out every possible continuation and assumes the opponent always plays perfectly.
- **Alpha-beta pruning:** while searching, the AI tracks the best score each side is already guaranteed. As soon as a branch can't beat that, the AI stops exploring it. The result is the same, with far fewer positions searched.

Since perfect play from both sides always ends in a draw, two AIs playing each other will always tie:

```
$ python main.py
...
['O', 'X', 'O']
['O', 'X', 'X']
['X', 'O', 'X']

It's a tie!
```

## Run it

**Play against the AI** in a graphical window:

```bash
pip install -r requirements.txt
python runner.py
```

> `runner.py` expects the font file `OpenSans-Regular.ttf` in the same folder. Download it from Google Fonts, or point it to any `.ttf` file.

**Watch the AI play itself** in the terminal:

```bash
python main.py
```

## Built with

Python · Pygame
