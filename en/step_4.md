## Shark health

In this step you will reduce the health of the shark, if it accidently eats any plastic waste.

--- task ---

Create a new `variable`{:class="block3variables"} called `health`{:class="block3variables"}

--- /task ---

--- task ---

On the **shark** sprite, when the game starts, the shark's health should be set to `0`{:class="block3variables"}, and then when the health gets below `0`{:class="block3variables"} the game should end.

![shark sprite](images/shark-sprite.png)

```blocks3
when flag clicked
go to x: (0) y: (-120)
+set (health v) to (0)
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

```blocks
when I start as clone
forever
if <touching (shark v)> then
change (health v) by (-5)
delete this clone
```
--- /task ---

--- save ---
