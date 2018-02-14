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

## 3 Predifined class
### 1 Restaurant
Party
- party  

Restaurant
- List<Table> tables
- List<Meal> menu  
- Table findTable()  


Table
- boolean available
- boolean isAvailable()
- void markUnavailable()

Order
- List<Meal> meals   
  
  
Meal
- sth


(stop at 30min)
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
- void shuffle()
- void dealInitialCards()
- Card dealNextCard()

Hand
- List<Card> cards
- void insertCard(Card c)

Player
- Hand hand
- int totalBets
- int currentBets
- Deck d
- Boolean stopDealing
- void joinGame(Deck d)
- void placeBets(int amount)  
- void insertCard(Card c)
- void dealNextCard()
- void stopDealing()  
- void updateBets(int amount)

Dealer
- Hand hand  
- Deck d
- int bets
- void insertCard(Card c)
- void dealNextCard()
- booean largerThan(Player p)
- void updateBets(n:amount)

Card
- int value

Design pattern:
- Sing
- Stragegy
- DAO
- Adapter
- State
- Decorator
- Factory

Three types of singleton:  
BASIC
```
public class ParkingLot
{
  private static ParkingLot _instance = null;
  private List<Level> levels;
  private ParkingLot(){
    levels = new ArrayList<level>();
  }
  public static ParkingLot getInstance(){
    if(_instance==null){
      _instance = new ParkingLot();
    }
    return _instance;
  }
}
```

Static internal
```
public class ParkingLot
{
  private ParkingLot(){}
  private static class LazyParkingLot{
    static final ParkingLot _instance = new ParkingLot();
  }
  public static ParkingLot getInstance()
  {
    return LazyParkingLot._instance;
  }
}
```
