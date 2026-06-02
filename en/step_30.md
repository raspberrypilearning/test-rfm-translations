<h2 class="c-project-heading--task">Add a fall-off-the-level danger</h2>

Treat falling below the level as a danger so the player has to stay on the safe route.

### Choose this route if...

You want the level itself to be dangerous, even without enemies or spikes.

### Notice when the player falls too low

Choose a y position lower than your floor or lowest platform, then use that value in the block below.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <(y position) < [fall y]> then
    broadcast [game over v]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Make the player fall below the level and check that the `game over` message runs.
