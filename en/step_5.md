## Feed the shark

At the moment, when you play the game, the shark needs to avoid the plastic or the game ends. In this step, you will add fish that the shark can eat to increase its health.

--- task ---

**Duplicate** the plastic sprite by right-clicking on the sprite and choosing **Duplicate** from the menu:

![A user interface showing a rectangular card labeled "Plastic" with an image of a plastic bottle on it. A circular button with a trash bin icon is positioned over the card's top right corner. A dropdown menu with options "duplicate," "export," and "delete" is open in the foreground. The menu has a purple background with white text.](images/dupe-plastic.png)

--- /task ---

--- task ---

Rename this 

--- /task ---

--- task ---

Click on the **Costumes** tab and add a new **Fish** costume to your new sprite:

![A vertical purple toolbar on the left side of the screen shows four icons: a crown, sparkles, a paintbrush, and a magnifying glass. At the bottom of the toolbar is a green circular button with a cat face icon, followed by a plus sign. A green tooltip next to the button reads "Choose a Costume."](images/choose-costume.png)
![A costume selection interface with a purple search bar at the top containing the search term "fish" and a magnifying glass icon. Below, two fish costume cards are displayed side by side. The left card shows an orange-and-white clownfish labeled "Fish-a," and the right card shows a blue-and-yellow fish labeled "Fish-b."](images/fish-costume.png)

--- /task ---

--- task ---

Delete the other costumes using the bin icon:

![A purple rectangular card labeled "Wrapper" with dimensions "201 x 200" displayed underneath a small illustration of a crumpled orange wrapper. The card has the number "4" in the top left corner, and a circular button with a trash bin icon is positioned over the card's top right corner.](images/delete-sprites.png)

--- /task ---

--- task ---

Now, you can edit the code that reduces the shark's health so that it increases its health by `1` instead:

![fish sprite](images/fish-sprite.png)

```blocks3
when I start as a clone
forever
if <touching (Shark v)> then
+ change (health v) by (1)
delete this clone
```

--- /task ---

--- task ---

Set the **Fish** sprite size property to `40` percent and the direction property to `180` degrees. 

![the size and direction properties for the fish sprite.](images/fish-properties.png)

--- /task ---

--- task ---

Run the program again to test that the health of the shark increases if it eats fish.

--- /task ---


--- save ---


