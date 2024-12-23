## Monitor the shark's health

Use a `variable`{:class="block3variables"} to include health points. The health of the shark will reduce if it accidentally eats plastic waste.

--- task ---

Create a new `variable`{:class="block3variables"} called `health`.

--- /task ---

--- task ---

Click on the **Shark** sprite in the Sprite list. Add blocks so that when the game starts, the shark's health is set to `20`, and when the shark's health goes below `0`, the game ends:

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+set (health v) to (20)
forever
if <mouse down?> then
if <(mouse x) < (x position)> then
change x by (-10)
end
if <(mouse x) > (x position)> then
change x by (10)
end
+if <(health) < (0)> then
stop (all v)
```

--- /task ---

--- task ---

Go back to the **Plastic** sprite. Add some code to reduce the shark's health by `-5` if it accidentally eats any of the plastic:

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (Shark v)> then
change (health v) by (-5)
delete this clone
```

--- /task ---

--- task ---

Run the program again to test that the health of the shark reduces if it eats plastic.

--- /task ---

--- save ---
