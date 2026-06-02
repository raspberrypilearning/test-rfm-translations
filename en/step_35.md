<h2 class="c-project-heading--task">Animate your player</h2>

Switch costumes while the player moves so the character feels more alive.

### Choose this route if...

You want the player to look more lively while moving around the level.

### Change costumes while the player moves

If your player only has one costume, duplicate it first and make a small change so the movement looks different.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    next costume
    wait (0.15) seconds
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    next costume
    wait (0.15) seconds
  end
end
```


### Next choices

Your player feels more alive now. Add sound, visual feedback, or test whether the animation matches the movement.

- Go to [Add sound effects](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/36)
- Go to [Add visual feedback](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/39)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Move the player and check that the costumes change while it moves.
