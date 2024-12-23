## Add plastic waste

Add plastic waste to your game, for the player to avoid.

In the Sprite list below the Stage, click on the sprite that looks like a plastic bottle. This sprite has four costumes: a bottle, a wrapper, a bag, and a plastic can holder.

--- task ---

When the green flag is clicked, the **Plastic** sprite needs to move to the top of the Stage and then `hide`{:class="block3looks"}. Add the following code to the **Plastic** sprite:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (200)
hide
```

--- /task ---

--- task ---

The **Plastic** sprite now needs to randomly generate clones of itself. Add the following code:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (200)
hide
+forever
create clone of (myself v)
wait (pick random (1) to (5)) seconds
```

--- /task ---

--- task ---

When a clone is created, the clone needs to `show`{:class="block3looks"} itself, pick a `random`{:class="block3operators"} `costume`{:class="block3looks"}, and then move to a `random`{:class="block3operators"} `x`{:class="block3motion"} position. Add the following code as a new script:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (200)
```

--- /task ---

--- task ---

You want the plastic to move towards the bottom of the Stage at a  `random`{:class="block3operators"} speed, so create a new `variable`{:class="block3variables"} called `speed`. Set it to `For this sprite only`:

![new variable menu](images/speed-variable.png)



--- /task ---

--- task ---

Set the `speed`{:class="block3variables"} to be a `random`{:class="block3operators"} number. Add a `set speed to`{:class="block3variables"} block below the `go to x: y:`{:class="block3motion"} block and set it to `pick random -1 to -10`.

![plastic sprite](images/plastic-sprite.png)
```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4))
go to x: (pick random (-200) to (200)) y: (200)
+set (speed v) to (pick random (-1) to (-10))
```

--- /task ---

--- task ---

Add a `repeat until`{:class="block3control"} block below the `set speed to`{:class="block3variables"} block. Use the condition `y position < -180` to detect when the clone reaches the bottom of the stage.

![plastic sprite](images/plastic-sprite.png)
```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4))
go to x: (pick random (-200) to (200)) y: (200)
set (speed v) to (pick random (-1) to (-10))
+repeat until <(y position) < (-180)>
end
```

--- /task ---

--- task ---

Inside the `repeat until`{:class="block3control"} block, add a `change y by`{:class="block3motion"} block and set it to `speed`{:class="block3variables"} to move the clone down the stage.

![plastic sprite](images/plastic-sprite.png)
```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4))
go to x: (pick random (-200) to (200)) y: (200)
set (speed v) to (pick random (-1) to (-10))
repeat until <(y position) < (-180)>
+change y by (speed)
end
```

--- /task ---

--- task ---

Below the `change y by`{:class="block3motion"} block, add a `wait`{:class="block3control"} block and set it to `0.1` seconds so the movement is visible.

![plastic sprite](images/plastic-sprite.png)
```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4))
go to x: (pick random (-200) to (200)) y: (200)
set (speed v) to (pick random (-1) to (-10))
repeat until <(y position) < (-180)>
change y by (speed)
+wait (0.1) seconds
end
```

--- /task ---

--- task ---

Test your code. 

Run your game by clicking the green flag, and you should see the plastic waste falling from random positions and at random speeds from the top of the Stage. The problem is that the waste accumulates at the bottom of the Stage, and stays there.

--- /task ---

--- task ---

Add a `delete this clone`{:class="block3control"} block so that the **Plastic** sprite deletes itself when it hits the bottom of the Stage:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (200)
set (speed v) to (pick random (-1) to (-10))
repeat until <(y position) < (-180)>
change y by (speed)
wait (0.1) seconds
end
+delete this clone
```

--- /task ---

--- save ---

