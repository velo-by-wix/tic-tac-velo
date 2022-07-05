## Importing your Backend Code

In this module, you'll see how easy it is to access backend functionality in your frontend with Velo. You will learn how to import backend web modules.

**:bulb: New concepts**
- [Importing Files](https://support.wix.com/en/article/velo-web-modules-calling-backend-code-from-the-frontend)


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
