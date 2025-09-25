## Move the shark

Add code to allow the player to use a mouse to control the motion of a shark on the Stage.

--- task ---

Open the [starter project](http://rpf.io/save-the-shark-on){:target="_blank"} in Scratch.


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


If the user clicks the mouse on the left-hand side of the **Shark** sprite's position, then the **Shark** sprite should move to the left.

--- task ---

Add an `if`{:class="block3control"} block inside the `forever`{:class="block3control"} loop, with the condition `mouse x`{:class="block3sensing"} is `less than`{:class="block3operators"} the `x position`{:class="block3motion"} of the **Shark** sprite.

![shark sprite](images/shark-sprite.png)
```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
+if <(mouse x) < (x position)> then
end
```

--- /task ---

--- task ---

Inside the `if`{:class="block3control"} block, add a `change x by`{:class="block3motion"} block and set the value to `-10` to move the **Shark** sprite to the left.

![shark sprite](images/shark-sprite.png)
```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
+change x by (-10)
end

```

--- /task ---


--- task ---

Add a `next costume`{:class="block3looks"} block to the end of your script, so the shark looks like it is swimming when it moves:

![shark sprite](images/shark-sprite.png)
```blocks3
when flag clicked
go to x: (0) y: (-120)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
change x by (-10)
+next costume
end
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
