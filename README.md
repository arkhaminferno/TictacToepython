# TictacToepython
Welcome to the TicTacToe Game,a simple Python Program allowing PVP(Player Vs Player) game mode."Machine-mode" is not required to be implemented.

# Players selection
When the game is loaded, X goes first(wil be the default first player)

## The board


      - | - | -       1 | 2 | 3
      - | - | -       4 | 5 | 6
      - | - | -       7 | 8 | 9
      
# Logic of the Program
  ## display board (Using List)
  ## Will hold our game board data
``  board = ["-", "-", "-",
         "-", "-", "-",
         "-", "-", "-"]
``

## Display the game board to the screen
```
def display_board():
   print("\n")
   print(board[0] + " | " + board[1] + " | " + board[2] + "     1 | 2 | 3")
   print(board[3] + " | " + board[4] + " | " + board[5] + "     4 | 5 | 6")
   print(board[6] + " | " + board[7] + " | " + board[8] + "     7 | 8 | 9")
   print("\n")
```
## play game
    Handle turn from one player to another
## 4.Check win
  `check rows`
  `check columns`
  `check diagonals`
  
  ```
  def check_for_winner():
  # Set global variables
  global winner
  # Check if there was a winner anywhere
  row_winner = check_rows()
  column_winner = check_columns()
  diagonal_winner = check_diagonals()
  # Get the winner
  if row_winner:
    winner = row_winner
  elif column_winner:
    winner = column_winner
  elif diagonal_winner:
    winner = diagonal_winner
  else:
    winner = None

```
# check tie
  ```
  # Check if there is a tie
def check_for_tie():
  # Set global variables
  global game_still_going
  # If board is full
  if "-" not in board:
    game_still_going = False
    return True
  # Else there is no tie
  else:
    return False
 ```


# Flip player
```#Flip the current player from X to O, or O to X
def flip_player():
  #Global variables we need
  global current_player
  #If the current player was X, make it O
  if current_player == "X":
    current_player = "O"
  #Or if the current player was O, make it X
  elif current_player == "O":
    current_player = "X"
 ```
    
 
# Help and Support
  [Author](https://www.linkedin.com/in/arkhaminferno/)
