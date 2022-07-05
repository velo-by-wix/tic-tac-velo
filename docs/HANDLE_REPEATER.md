## Handling a Repeater

In this module, you'll learn how to work with Repeaters in Velo.

**:bulb: New concepts**
- [Repeater](https://www.wix.com/velo/reference/$w/repeater) Editor Element


**:white_check_mark: Step-by-Step Instructions**

1. Back in the IDE, go to the HOME file. Delete the comments (any line of code that starts with //).

2. At the top of the HOME file, import the board from the backend.
```JavaScript
import { board } from 'public/game-logic.js'
```

3. Create a variable to track the game state, below this import.
```JavaScript
let state = {
   player: 'X',
   board,
   winner: null
}
```

:fast_forward: Next Module => [Handling a Repeater](HANDLE_REPEATER.md)
