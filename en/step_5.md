## Feed the shark

Now when you play the game, the shark needs to avoid the plastic or the game end. In this step, you'll add fish that the shark can eat to increase it's health.

--- task ---

Add the fish sprite to your project.

![image showing search and selection of fish sprite](images/add-fish.png)

--- /task ---

The code for the fish sprite is almost identical to the code on the plastic sprite.

--- task ---

Drag and drop the three scripts from the plastic sprite onto the fish sprite.

![copy scripts](images/copy-scripts.gif)

--- /task ---

--- task ---
Now you can edit the code that reduces the shark's health so that it increases the health instead.

![fish sprite](images/fish-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (shark v)> then
+ change (health v) by (1)
delete this clone
```

--- /task ---

--- save ---


