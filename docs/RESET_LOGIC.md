## Reset the Board

In this module, you'll use logic to determine if and when someone has won the game. You will use that state to show a winner's box.

**:white_check_mark: Step-by-Step Instructions**

1. The final steps here are to add functionality that resets the board after a game is won, or when the players choose to (usually because of a draw). First, add the following code to the _game-logic.js_ file.
```JavaScript
export const resetBoard = (state) => {
   // reset board state
   state.board.forEach((item) => { item.piece = "" })
   // update board text
   $w("#repeater1").forEachItem(($item, itemData, index) => {
       $item("#square").label = itemData.piece
       $item("#square").enable()
   })
}
```

2. Add resetBoard to the import at the top of the _HOME_ page.
```JavaScript
import { board, calculateWinner, squarify, resetBoard } from 'public/game-logic.js'
```

3. Then add the following code to the end of the showWinner() function.
```JavaScript
resetBoard(state);
```

4. Next add a button to your page to allow for a manual reset of the game board. (I created one with an ID of #resetButton). Add an onClick() functionality to this button, and inside the button add the following code. Note: Don’t attach the button to your game board.
```JavaScript
resetBoard(state);
```

5. Finally, add a close button attached to your winnerBox. Give it on click functionality to hide the winner box when clicked.
```JavaScript
$w('#winnerBox').hide()
```

7. Go ahead and publish your application to play Tic Tac Velo!

:boom: **Hurray! You've completed the challenge. You have now acquired the skills to create your own web application using Velo!** :confetti_ball:
