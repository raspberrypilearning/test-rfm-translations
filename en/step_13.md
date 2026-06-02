<h2 class="c-project-heading--task">Add walls or boundaries</h2>

Stop the player from leaving the level by adding walls or simple boundary checks.

### Choose this route if...

You want to keep a climbing, maze-like, or scrolling game inside a clear play area.

### Keep the player inside the level

Paint tall wall sprites with the `Platform` sprite, or use the boundary checks below once your player can move.

Add this code to the Player sprite:

```blocks3
if <(x position) > [220]> then
  set x to [220]
end
if <(x position) < [-220]> then
  set x to [-220]
end
```


### Next choices

Now that the player stays in bounds, choose a movement route or shape the level around those boundaries.

- Go to [Make your player climb ladders](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/16)
- Go to [Make your player follow the mouse](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/17)
- Go to [Make a scrolling level](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/19)

<h2 class="c-project-heading--task">Test</h2>

Move the player to the left and right edges and check that it stays inside the Stage.
