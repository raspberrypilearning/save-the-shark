## Move the shark

In this step, you will add code to allow the player to use a mouse to control the motion of a shark on the Stage.

--- task ---

**Online:** open the [starter project](http://rpf.io/save-the-shark-on){:target="_blank"} in Scratch.
 
**Offline:** open the [project starter file](https://rpf.io/p/en/save-the-shark-go){:target="_blank"} in the Scratch offline editor. If you need to, you can [download and install Scratch here](https://scratch.mit.edu/download){:target="_blank"}.

--- /task ---

In the starter project, you should see a **Shark** sprite, against an underwater background.

![starter project](images/starter_project.png)

--- task ---

When the green flag is clicked, the shark needs to start at the bottom of the Stage. Add this code so that the **Shark** sprite starts in the correct position:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
```

--- /task ---

To make this project suitable for mobile devices, you will use the location of the cursor when the left mouse button is pressed, or when a finger touches the screen, to control the movement of the shark. Luckily, Scratch's `mouse down`{:class="block3sensing"} block works for fingers on mouse buttons and on touchscreens!

--- task ---

Your program needs to continuously detect when the left mouse button is pressed. To do this, add a `forever`{:class="block3control"} loop to your script, then use an `if ... then`{:class="block3control"} block to detect if `mouse down`{:class="block3sensing"}:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+forever
if <mouse down?> then
```

--- /task ---

--- task ---

If the user clicks the cursor closer to the left-hand side of the Stage than the **Shark** sprite's position, then the **Shark** sprite moves to the left.

This action is possible because the position of the cursor along the x axis is stored in the `mouse x`{:class="block3sensing"} block.

To get the program to respond to where the user clicks, add the following blocks: `if`{:class="block3control"} `mouse x`{:class="block3sensing"} is `less than`{:class="block3operators"} the `x position`{:class="block3motion"} of the **Shark** sprite, `then`{:class="block3control"} the sprite should `change x by`{:class="block3motion"} `-10` to move to the left:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
+if <(mouse x) < (x position)> then
change x by (-10)
next costume
```

--- /task ---

--- task ---

Click on the green flag to run the program to test that the shark moves to the left when you click to the left of the shark.

--- /task ---

--- task ---

When the mouse is clicked, `if`{:class="block3control"} `mouse x`{:class="block3sensing"} is `greater than`{:class="block3operators"} the `x position`{:class="block3motion"}, `then`{:class="block3control"} the **Shark** sprite should `change x by`{:class="block3motion"} `10` to move to the right. Add the following blocks:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
change x by (-10)
next costume
end
+if <(mouse x) > (x position)> then
change x by (10)
next costume
```

--- /task ---

--- task ---

Click on the green flag to run the program to test that the shark moves to the right when you click to the right of the shark.

--- /task ---

--- save ---
