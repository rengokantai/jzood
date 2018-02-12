# nt_jzood

Open close principle
open to extension, close to modification

Interface segregation principle

Dependency inversion principle

===
Clarify
Core objects
Cases
Classes
Correctness




## 5 Design Game
### 1 Tic tac toe.
Tictactoe: 
- Board board
- Char CurrentMove='X'
- void() changePlayer()
Board: 
- char[][] board
- void initializeBoard[]
- void makeMove(n: row,int col, char currentMove)
- boolean checkWin()
- boolean isBoardFull()


### 2 Chinese.  

Player
- Name
- Points
- updatePoints(int diff)  

Chinese Chess
- List<Game> games  
  
Game  
- Player redPlayer
- Player blackPlayer
- Piece[][] board
- void joinGame(Player p)
- void initializaBoard()
- boolean move(Piece piece, int row,int col) 
- void changePlayer()
- boolean ifCurrentPlayerWin()
- void gameDraw()
  
  
Piece  
- Color color
- Role role  

<Enum> Color
- Black
- Red  
  
<Enum> Role
- ROOK
- OTHER


#### Use case:
- Initialization

### 3. Blackjack
Note, all other types of OOD except blackjack relys on the entity except card game, which relys on designing most propertys and methods
on player.  

Deck
- Dealer dealer
- List<player> players
- void addPlayer(Player p)

Hand
- List<Card> cards

Player
- Hand hand
- int totalBets
- int currentBets
- void joinGame(Deck d)
- void placeBets(int amount)  

Dealer
- Hand hand  

Card
