## Flipping State

In this module, you'll use logic to flip the value of the state.

**:bulb: New concepts**
-


**:white_check_mark: Step-by-Step Instructions**

1. Create a new turnover function on the HOME page in your IDE after the onReady() function.
```JavaScript
export function turnover() {
   state.player === 'X' ? state.player = 'O' : state.player = 'X'
}
```

2. Call your turnover() function at the end of your button’s square_click() function.
```JavaScript
// change turn
turnover()
```

3. Now when you preview your site, you should be able to click the buttons and see alternating Xs and Os placed on the board.

:fast_forward: Next Module => [Find the Winner!](FIND_WINNER.md)
