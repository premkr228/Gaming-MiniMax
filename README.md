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
<br>Board is a 7-column × 6-row grid.</br>
<br>Discs drop to the lowest available space in the selected column.</br>
<br>Turn-based gameplay: human player first, AI follows.</br>
<br>Win condition: Four connected discs horizontally, vertically, or diagonally.</br>
<br>Draw occurs when the board is full without a winner.</br>

# AI Strategy (Minimax Algorithm)
<br>Evaluates possible future states to a fixed depth.</br>
<br>Prioritizes winning or blocking moves immediately.</br>
<br>Scoring heuristics evaluate board favorability.</br>
<br>Recursively simulates future states to select the optimal move.</br>

# Static Evaluation Heuristic
<br>The AI scores the board based on:</br>
### Center Column Control:
   <br> +3 per AI disc (central control boosts connectivity).</br>
### Four-cell sliding windows:
   <br> +100 for 4 AI pieces (win)</br>
   <br> +5 for 3 AI + 1 empty (strong opportunity)</br>
   <br> +2 for 2 AI + 2 empty (moderate)</br>
   <br> -4 for 3 opponent + 1 empty (block)</br>
### Example Score Analysis (Score: -3):
   <br> Center control: +3</br>
   <br> Player horizontal advantage: -5</br>
   <br> AI moderate opportunities: +2</br>
   <br> Diagonal threats: -3</br>

# User Interaction
<br>User inputs column number (0–6) via terminal.</br>
<br>AI counters using Minimax strategy.</br>
<br>Board updates shown after each move.</br>
### <br>Discs:</br>
   <br> Red: Human Player</br>
   <br> Yellow: AI</br>
### <br>Latest move:</br>
    <br>Human: yellow border</br>
    <br>AI: black border</br>

# Edge Case Handling
<br>Prevents invalid inputs (e.g., non-numeric or out-of-range).</br>
<br>Avoids full column selections.</br>
<br>Graceful exit on keyboard interruption.</br>

# Visualization
<br>Board displayed via Matplotlib.</br>
<br>Differentiated highlights for user and AI moves.</br>
<br>Dual-view: player’s move (left), AI’s response (right).</br>
