<h2 class="c-project-heading--task">Add walls or boundaries</h2>

Stop the player from leaving the level by adding walls or simple boundary checks.

### Choose this route if...

You want to keep a climbing, maze-like, or scrolling game inside a clear play area.

### Keep the player inside the level

Paint tall wall sprites with the `Platform` sprite, or use the boundary checks below once your player can move. Change the edge values so they match the left and right limits of your own level.

Add this code to the Player sprite:

```blocks3
if <(x position) > [right edge]> then
  set x to [right edge]
end
if <(x position) < [left edge]> then
  set x to [left edge]
end
```


<h2 class="c-project-heading--task">Test</h2>

Move the player to the left and right edges and check that it stays inside the Stage.
