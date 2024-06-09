---
title: Checker  
date: 2024-06-09 12:02:09 +/-TTTT
categories: [Project, Game]
tags: [python, raylib, game]
---

### Project Overview

The Checker game is a classic board game where two players take turns to move their pieces diagonally on an 8x8 board. The main features of my implementation include:

- **User Interface:** A simple, intuitive UI with a visually appealing board and pieces.
- **Game Logic:** Rules for valid moves, capturing opponent pieces, and kinging.
- **Turn-Based Play:** Alternating turns between two players.
- **Winning Conditions:** Detecting when a player wins the game.

## How to run 
```console
$ ./build.sh
```
## Implementation 
- This project use `python` programming language and for graphics it uses `raylib`.\
- `gui_version.py` contains all the implementation of game 
### Implementation structure 
- `main`: is main game loop
- `init_game`: initialize an empty grid and set all variable to zero 
- `get_moves`: it accepts row and col of cell and grid to calculate the valid move for particular piece 


## Demo 
<center>
<img title="a title" alt="Alt text" src="/assets/blog-data/img/2024-06-09-checker-game/demo-1.png" width=380px>
<img title="a title" alt="Alt text" src="/assets/blog-data/img/2024-06-09-checker-game/demo-2.png" width=380px>
</center>