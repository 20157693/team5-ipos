# Tic Tac Toe Flask Application

A simple Tic Tac Toe game built with Python and Flask. This application allows two players to play Tic Tac Toe in a web browser.

## Features

- Two-player Tic Tac Toe game
- Simple web interface
- Option to reset the game

## Getting Started

### Prerequisites

- Python 3.x
- pip (Python package installer)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/tic-tac-toe.git
   cd tic-tac-toe
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application:**

   ```bash
   python app.py
   ```

4. **Open your web browser:**

   Go to `http://127.0.0.1:5000` to play the game.



## Group Process
1. Before working on anything or deciding on what to work on, please check and review completed issues as to make sure you aren't working on a task thats already been completed

2. If working on a feature/bug, create it in the issues panel first so others don't double up on work or work on the same segment of code you are working on.

3. When completed, submit it through PR and wait for confirmation/reviewing from at least 3 members.
   - If not passed, review feedback and apply it, then repeat the previous step.

4. When successfully reviewed, confirm the PR and mark the issue as complete.



## Undo Last Move Feature

The Tic Tac Toe game includes an **Undo Last Move** feature.

This feature uses a stack data structure called `move_history`.

### How it works

- When a player makes a valid move, the move is pushed onto the `move_history` stack.
- Each stack item stores the board cell and the player who made the move.
- When the user clicks **Undo Last Move**, the most recent move is popped from the stack.
- The selected board cell is cleared.
- The current player is changed back to the player who made the undone move.
- When the game is reset, the stack is cleared.

### Requirement covered

This feature satisfies the requirement for:

```text
stack/queues/linked lists & hashing
```
### Testing

Unit tests were added in:

```text
tests/test_undo_stack.py
```
The tests check that:

- A move is added to the stack.
- Undo removes the most recent move.
- Reset clears the stack.
