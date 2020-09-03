## Plastic waste

You should see a sprite that looks like a plastic bottle, in your sprites panel beneath the stage. This sprite has four costumes: a bottle, a wrapper, a bag and a can holder.

--- task ---

When the flag is clicked, this sprite needs to move to the top of the screen and then `hide`{:class="block3looks"} itself. Add the following code:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (200)
hide
```

--- /task ---

--- task ---

The plastic sprite should now randomly generate clones of itself.

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

When a clone is created, it should `show`{:class="block3looks"} itself, pick a random costume, and then  move to a random `x`{:class="block3motion"} position. Add the following code as a new script:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (0)
```
--- /task ---

--- task ---

You want the speed that the plastic moves towards the bottom of the screen to be `random`{:class="block3operators"}, so create a new `variable`{:class="block3variables"} called `speed`{:class="block3variables"}.

--- /task ---

--- task ---

Set the `speed`{:class="block3variables"} to be a `random`{:class="block3operators"} number, and then move the clone down the stage using the `speed`{:class="block3variables"} variable:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (0)
+set (speed v) to (pick random (-1) to (-10))
+forever
change y by (speed)
wait (0.1) seconds

```

--- /task ---

Run your game, and you should see the plastic waste falling from random positions and at random speeds from the top of the screen. The problem is that the waste accumulates at the bottom of the screen, and stays there.

--- task ---

Add blocks to detect when the plastic sprite hits the bottom of the screen, and then deletes itself:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
show
switch costume to (pick random (1) to (4)
go to x: (pick random (-200) to (200)) y: (0)
set (speed v) to (pick random (-1) to (-10))
forever
change y by (speed)
wait (0.1) seconds
+if <(y position) < (-180)> then
delete this clone
```

--- /task ---

--- save ---

