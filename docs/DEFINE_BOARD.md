## Define the board

In this module, you'll enable Dev Mode, also known as Velo. With Velo, you can add JavaScript code to your site and start to build out your application.

**:bulb: New concepts**
- [Enabling your Developer Environment](https://support.wix.com/en/article/about-velo-by-wix)


**:white_check_mark: Step-by-Step Instructions**

1. Turn on Dev Mode. When you do, you will notice that we now have a Velo sidebar on the left side of our screen and a **Properties and Events** panel on the right side of your IDE.

2. Change the ID of your button. First, click on your button. This should bring up the **Properties and Events** panel on the right side of your IDE. There is an ID field for the button. Change the ID from `button1` to `square`.

3. Attach the button to the first repeater item. This should populate the repeater with 9 identical copies of the button.

4. Go to the Public & Backend { } section of the Velo sidebar and create a game-logic.js public file.

5. Clear the code in the game-logic.js file, then add the following code to the file. This code represents the game board.
```JavaScript
export const board = [
   {
     "_id":"0",
     "piece":""
   },
   {
     "_id":"1",
     "piece":""
   },
   {
     "_id":"2",
     "piece":""
   },
   {
     "_id":"3",
     "piece":""
   },
   {
     "_id":"4",
     "piece":""
   },
   {
     "_id":"5",
     "piece":""
   },
   {
     "_id":"6",
     "piece":""
   },
   {
     "_id":"7",
     "piece":""
   },
   {
     "_id":"8",
     "piece":""
   }
];
```



:fast_forward: Next Module => [Import backend Code](IMPORT_BE.md)
