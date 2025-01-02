Single Second Chess Bot
This repository contains a Python-based chess bot designed for the Single Second Chess competition. The bot evaluates chess positions and selects the best possible move using a simple evaluation strategy, focusing on efficiency and computational constraints.

Features
Input: Accepts chess positions in Forsyth-Edwards Notation (FEN).
Output: Outputs the best move in Universal Chess Interface (UCI) format.
Evaluation: Uses a material-based heuristic to score moves.
Efficiency: Designed to operate within strict computational limits.
How It Works
Input: The bot reads a FEN string representing the chessboard's state from standard input.
Processing:
The python-chess library initializes the board and generates legal moves.
Moves are evaluated using a material scoring function.
The move with the highest score is selected.
Output: The chosen move is printed in UCI format (e.g., e2e4).
Installation
Prerequisites
Python 3.7 or higher
python-chess library
Installation Steps
Install Python (if not already installed).
Install the required library:
bash
Copy code
pip install python-chess
Usage
Save the bot code to a file named single_second_chess.py.
Run the bot from the command line or terminal by providing a FEN string.
Example Command
bash
Copy code
echo "rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1" | python single_second_chess.py
Example Output
plaintext
Copy code
e2e4
Code Overview
Functions
evaluate_board(board):

Scores the board based on material values (e.g., pawn = 1, queen = 9).
Favors positions advantageous to the current player.
get_best_move(fen):

Iterates through legal moves.
Evaluates each move and selects the one with the highest score.
main():

Reads input, processes the board, and outputs the best move.
File Structure
plaintext
Copy code
single_second_chess.py   # Main script for the chess bot
README.md                # Project documentation
Example Walkthrough
Input:

bash
Copy code
rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1
This FEN string represents the starting position of a chess game.
Processing:

The bot evaluates all possible moves.
It selects the move with the highest material advantage.
Output:

Copy code
e2e4
Customization
Improve Evaluation:
Add heuristics for positional play, mobility, and king safety.
Advanced Algorithms:
Implement Minimax or Alpha-Beta Pruning for deeper game tree analysis.
Performance:
Optimize code for speed to meet computational limits.
Limitations
The bot currently uses a greedy approach, evaluating one move at a time.
Advanced strategies and deeper evaluations are constrained by computational limits.
Future Enhancements
Optimize the evaluation function for speed and accuracy.
Implement iterative deepening to balance depth and efficiency.
Add support for common chess strategies and opening databases.
License
This project is licensed under the MIT License. See the LICENSE file for details.
