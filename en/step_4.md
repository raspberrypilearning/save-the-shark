## Shark health

In this step, you will use a `variable`{:class="block3variables"} to include health points. The health of the shark will reduce if it accidentally eats plastic waste.

--- task ---

Create a new `variable`{:class="block3variables"} called `health`.

--- /task ---

--- task ---

On the **Shark** sprite, when the game starts, the shark's health should be set to `20`, and then when the health gets below `0`{:class="block3variables"} the game should end.

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

Back on the **Plastic** sprite, add some code to reduce the shark's health if it accidently eats any of the plastic.

![plastic sprite](images/plastic-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (shark v)> then
change (health v) by (-5)
delete this clone
```
--- /task ---

--- task ---

Run the program again to test that the health of the shark reduces if it eats plastic.

--- /task ---

--- save ---
