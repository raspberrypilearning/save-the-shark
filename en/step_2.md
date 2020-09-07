## Move the shark

In this step, you will use code to control the motion of a shark on the Stage using the mouse.

--- task ---

**Online:** open the [starter project](http://rpf.io/save-the-shark-on){:target="_blank"} in Scratch.
 
**Offline:** open the [project starter file](http://rpf.io/p/en/save-the-shark-get){:target="_blank"} in the Scratch offline editor. If you need to, you can [download and install Scratch here](https://scratch.mit.edu/download){:target="_blank"}.


![starter project](images/starter_project.png)

--- /task ---

In the starter project, you should see a **Shark** sprite, against an underwater background.

--- task ---

When the green flag is clicked, the shark should start at the bottom of the screen. Add this code so that the shark starts in the correct position.

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
```

--- /task ---

To make this project suitable for mobile devices, you will use the location of the cursor when the left mouse button is pressed, or when a finger touches the screen, to control the movement of the shark.

--- task ---

Add a `forever`{:class="block3control"} loop to your script, so that your program can constantly detect when the left mouse button is clicked, then use an `if ... then`{:class="block3control"} block to detect if `mouse down?`{:class="block3sensing"}.

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+forever
if <mouse down?> then
```

--- /task ---

--- task ---

When the mouse is clicked, if the `mouse x`{:class="block3sensing"} position of the cursor is `less than`{:class="block3operators"} the `x position`{:class="block3motion"} of the sprite, then the sprite should `change x by`{:class="block3motion"}`-10` to move to the left. Add the following blocks:

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

Click on the green flag to run the program to test that the shark moves to the left.

--- /task ---

--- task ---

If the `mouse x`{:class="block3sensing"} position of the cursor is `greater than`{:class="block3operators"} the `x position`{:class="block3motion"} of the sprite, then the sprite should `change x by`{:class="block3motion"}`10` to move to the right. Add the following blocks:

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

Click on the green flag to run the program to test that the shark moves to the right.

--- /task ---

--- save ---
