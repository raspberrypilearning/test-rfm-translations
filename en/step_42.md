<h2 class="c-project-heading--task">Start another level</h2>

Use a new backdrop or layout so the player can continue into a second level.

### Choose this route if...

You want to turn one platformer challenge into a bigger adventure.

### Move on to level two

Make a second backdrop or a new set of platforms first. Then change your first win route so it broadcasts `next level` instead of `win` when the first level is finished. Use the name of your second backdrop in the block below.

Add this code to the Stage:

```blocks3
when I receive [next level v]
switch backdrop to [your level 2 backdrop v]
broadcast [start game v]
```


<h2 class="c-project-heading--task">Test</h2>

Trigger the `next level` message and check that the Stage switches to the new level and starts it.
