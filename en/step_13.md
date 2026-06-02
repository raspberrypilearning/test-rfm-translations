<h2 class="c-project-heading--task">Add walls or boundaries</h2>

Stop the player from leaving the level by adding walls or simple boundary checks.

### Choose this route if...

You want to keep a climbing, maze-like, or scrolling game inside a clear play area.

### Keep the player inside the level

Paint tall wall sprites with the `Platform` sprite, or use the boundary checks below once your player can move. On the Scratch Stage, the left edge is `x = -240` and the right edge is `x = 240`.

Add this code to the Player sprite:

```blocks3
if <(x position) > [240]> then
  set x to [240]
end
if <(x position) < [-240]> then
  set x to [-240]
end
```


<h2 class="c-project-heading--task">Test</h2>

Move the player to `x = -240` and `x = 240` and check that it stays inside the Stage.
