## Handling a Repeater

In this module, you'll learn how to work with Repeaters in Velo.

**:bulb: New concepts**
- [Repeater](https://www.wix.com/velo/reference/$w/repeater) Editor Element


**:white_check_mark: Step-by-Step Instructions**

1. Inside the onReady function, handle the creation of new repeated items and set the repeater data.
```JavaScript
// handle creation of new repeated items
$w("#repeater1").onItemReady(($item, itemData, index) => {
    $item("#square").label = itemData.piece;
});

// set the repeater data, triggering the creation of new items
$w("#repeater1").data = state.board
```

2. Select the repeater item, ‘square’. In the Properties and Events section on the right side of the IDE, add an onClick() event handler for your button. You should end up with something that looks like this:
```JavaScript
export function square_click(event) {
   // This function was added from the Properties & Events panel. To learn more, visit http://wix.to/UcBnC-4
   // Add your code for this event here:
}
```

3. Add functionality to the button’s onClick function to update the state and the button’s label, by changing the code within the square_click function.
```JavaScript
let $item = $w.at(event.context);
// change text
state.board[event.context.itemId].piece = $item("#square").label = `${state.player}`
// disable button on click
$item("#square").disable()
```

4. If you preview your site, you should be able to click each repeater item, adding an X to each one clicked. We need to add logic that will change the turn, and alternate which letter is placed onto the game board with each click.

:fast_forward: Next Module => [Flipping State](FLIP_STATE.md)
