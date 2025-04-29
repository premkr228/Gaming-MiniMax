![ricardo_vargas_2023_07_24_minimax 600x0-u1i0s1q90f1](https://github.com/user-attachments/assets/cea20b2d-55b4-4097-869e-5262c919b1fd)

# Gaming-MiniMax
The project implements a command-line-based Connect Four game where a human player competes against an AI. The AI employs the Minimax algorithm to make strategic decisions, with the game board visually represented using Matplotlib for clarity and engagement.

# Features
<br>7x6 grid where players drop discs in turns.</br>
<br>Automatic detection of winning conditions.</br>
<br>AI uses depth-limited Minimax with strategic evaluation.</br>
<br>Board visualization using Matplotlib with move highlights.</br>
<br>Handles invalid input and interruptions gracefully.</br>

# Game Mechanics
Board is a 7-column × 6-row grid.
Discs drop to the lowest available space in the selected column.
Turn-based gameplay: human player first, AI follows.
Win condition: Four connected discs horizontally, vertically, or diagonally.
Draw occurs when the board is full without a winner.

# AI Strategy (Minimax Algorithm)
Evaluates possible future states to a fixed depth.
Prioritizes winning or blocking moves immediately.
Scoring heuristics evaluate board favorability.
Recursively simulates future states to select the optimal move.

# Static Evaluation Heuristic
The AI scores the board based on:
## Center Column Control: 
    +3 per AI disc (central control boosts connectivity).
## Four-cell sliding windows:
    +100 for 4 AI pieces (win)
    +5 for 3 AI + 1 empty (strong opportunity)
    +2 for 2 AI + 2 empty (moderate)
    -4 for 3 opponent + 1 empty (block)
## Example Score Analysis (Score: -3):
    Center control: +3
    Player horizontal advantage: -5
    AI moderate opportunities: +2
    Diagonal threats: -3

# User Interaction
User inputs column number (0–6) via terminal.
AI counters using Minimax strategy.
Board updates shown after each move.
Discs:
    Red: Human Player
    Yellow: AI
Latest move:
    Human: yellow border
    AI: black border

# Edge Case Handling
Prevents invalid inputs (e.g., non-numeric or out-of-range).
Avoids full column selections.
Graceful exit on keyboard interruption.

# Visualization
Board displayed via Matplotlib.
Differentiated highlights for user and AI moves.
Dual-view: player’s move (left), AI’s response (right).
