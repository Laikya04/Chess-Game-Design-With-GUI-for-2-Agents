# Chess Game Using AI For 2-Agents

This is a chess game developed using Python and Pygame. The game features an interactive graphical interface for playing chess against a computer opponent. The AI opponent uses the Minimax algorithm with alpha-beta pruning for decision-making.
## Objective
The objective of this project is to develop a fully functional chess game using Python and Pygame, featuring an AI opponent that utilizes the Minimax algorithm with alpha-beta pruning. The game aims to provide a seamless and interactive user experience, allowing players to enjoy a classic game of chess against a computer opponent. The project also serves as a learning tool for understanding game development concepts, artificial intelligence, and algorithm implementation. Through this project, we aim to:

  - Implement a visually appealing and user-friendly graphical interface for the chessboard and pieces.
  - Develop an efficient and intelligent AI opponent capable of making strategic moves.
  - Enhance programming skills in Python and Pygame.
  - Gain a deeper understanding of game theory and the Minimax algorithm.
  - Create a modular and well-documented codebase for future enhancements and contributions.
   
## Demo


  ![Alt Text](https://media.giphy.com/media/hojJHfOF6Z8XvfHjl2/giphy.gif)
## Technologies Used

- Python
- Pygame
- python-chess
## Features

- Color selection
- Interactive UI using [pygame](https://www.pygame.org/)
- Configure search depth
- invalid move prevention 
- Interactive chessboard with draggable pieces.
- AI opponent using Minimax algorithm.
- Options to choose player color (white or black).
- Game over screen with options to play again or quit.
- Displays possible moves for selected pieces.
- Dynamic game evaluation for optimal moves.
  

## Usage

### 1. Setting Up the Game

- The game initializes with a main menu where you can choose to play as either white or black.
- Select your color by clicking the "WHITE" or "BLACK" button. The game will start immediately after selection.
### 2. Making Moves

- Click on a piece to select it. Possible moves will be highlighted.
- Click on a highlighted square to move the selected piece there.
- Right-click to deselect a piece if you change your mind.
### 3. AI Opponent

- After making your move, the AI opponent will calculate and make its move automatically.
- The difficulty of the AI can be adjusted by changing the depth of the Minimax algorithm.
### 4. Game Over

- If a checkmate or stalemate occurs, the game over menu will appear.
- You can choose to restart the game or quit.
## Algorithms Used
### 1. MiniMax

Minimax is a kind of backtracking algorithm that is used in decision making and game theory to find the optimal move for a player, assuming that your opponent also plays optimally. It is widely used in two player turn-based games such as Chess or Tic-Tac-Toe
In Minimax the two players are called maximizer and minimizer. The maximizer tries to get the highest score possible while the minimizer tries to do the opposite and get the lowest score possible.
Every board state has a value associated with it. In a given state if the maximizer has upper hand then, the score of the board will tend to be some positive value. If the minimizer has the upper hand in that board state then it will tend to be some negative value. The values of the board are calculated by some heuristics which are unique for every type of game.

![Alt Text](https://upload.wikimedia.org/wikipedia/commons/6/6f/Minimax.svg)

### 2. Evauation function

The evaluation function is used to assign a numerical value to a board state so that different board states that is a result of different sequence of moves could be compared by the MiniMax algorithm 

#### Factors that are considered
- Material
- Piece development

### 3. Alpha-beta pruning
This is an optimization algorithm that greatly reduces the number of board states that bahve to be evaluated by removing board states that are obviously undesireble

## Files Description
**1. Image directory :**

Contains all the images of the chess pieces.

**2. Board.py :** 

In this file we create a class of chessBoard and initialize and declare a 2D array of gametiles with null pieces and then place all the chess pieces on the board on their respective starting positions.

**3. Evaluation.py :** 

In this we define some of the special cases in chess for example castling, en passant rule, check. functions are used to check whether the player is in check, return moves available in case the player is in check, return moves in case of castling and return moves available in case of enpassant rule. It creates a Tile class which is placed on a chessboard array. It can store a position number on the board and a chess piece object.

**4. Pieces_Development_Values.py :** 

Contains files in which every chess piece class is defined. Every chess piece class has alliance (indicating whether the piece is white or black) and position ( coordinates on the chessboard ) attributes. It also has a legal move method which is used to calculate the legal moves for that chess piece on the chessboard.

**5. MiniMax.py :** 

Contains the logic for the AI algorithm. The AI was implemented using a recursive Minimax algorithm with alpha beta pruning and with the depth search of 3. The evaluation function assigned each chess piece a value, White pieces were assigned a positive value based on their rank and black pieces were assigned negative values based on their rank as well. So the total value becomes 0 in the start of the game where each side has all the pieces. The algorithm tried to search all possible moves up to the depth of 3 and calculate which next move could allow it to have the best evaluation value.

**6. main.py :** 

Main file of the program which merges all the functionality from the other files and itself as well to implement all this on pygame GUI.

## Future Work Possible

### 1. Online Multiplayer Mode:

  - Implement an online multiplayer mode allowing users to play against each other over the internet using technologies like WebSockets for real-time communication.
### 2. Improved AI:

  - Enhance the AI with advanced techniques such as neural networks or machine learning to make the AI more challenging and adaptable, and implement different difficulty levels.
### 3. User Profiles and Statistics:

  - Add user profiles to track player statistics, such as wins, losses, and draws, and implement an Elo rating system for players.
### 4. Move Analysis and Hints:

  - Provide move analysis and hints to help players improve their game and implement a feature to show the best move suggestions.
### 5. Game Replay and Analysis:

  - Enable players to save and replay their games, and offer tools to analyze completed games and identify mistakes.
