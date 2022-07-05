## Finding the Winner!

In this module, you'll use logic to determine if and when someone has won the game. You will use that state to show a winner's box.

**:bulb: New concepts**
-


**:white_check_mark: Step-by-Step Instructions**

1. Next we need to determine when a player wins the game. Back inside the _game-logic.js_ public file, we need to add the following code to calculate the winner.
```JavaScript
export const calculateWinner = (squares) => {
 const lines = [
   [0, 1, 2],
   [3, 4, 5],
   [6, 7, 8],
   [0, 3, 6],
   [1, 4, 7],
   [2, 5, 8],
   [0, 4, 8],
   [2, 4, 6],
 ];
 for (let i = 0; i < lines.length; i++) {
   const [a, b, c] = lines[i];
   if (squares[a] && squares[a] === squares[b] && squares[a] === squares[c]) {
     return squares[a];
   }
 }
 return null;
}
```

2. We also need to add a helper function to the _game-logic.js_ file that turns our game state into an array of pieces (Xs and Os).
```JavaScript
export const squarify = (array) => { return array.map(({ piece }) => piece) }
```

3. Back in our _HOME_ file, we need to update our import at the top of the page.
```JavaScript
import { board, calculateWinner, squarify } from 'public/game-logic.js'
```

4. Before we add these functions to our turnover() function, we must first include a way to actually display the winner of the game. Add a new container box over your game board. (I gave mine an ID of #winnerBox). Set the default value of this box to hidden.

5. Add a text field to the box. (I gave this an ID of #winnerText).

6. In your HOME file, create a function that will display the winner of a game.
```JavaScript
function showWinner(state) {
   $w('#winnerBox').show()
   $w('#winnerText').text = `${state.winner} wins!`
}
```

7. Now update the turnover() function to call our showWinner() function when a game winner has been determined.
```JavaScript
let winner = calculateWinner(squarify(state.board))
   if (winner) {
       state.winner = winner;
       showWinner(state);
       return;
   }
```

8. Now if you preview the game, you should have the winnerBox display when the game is won.

:fast_forward: Next Module => [Reset the board](RESET_LOGIC.md)
