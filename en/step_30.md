<h2 class="c-project-heading--task">Add a fall-off-the-level danger</h2>

Treat falling below the level as a danger so the player has to stay on the safe route.

### Choose this route if...

You want the level itself to be dangerous, even without enemies or spikes.

### Notice when the player falls too low

Choose a y position lower than your floor or lowest platform. The value below is a good starting point for many Scratch projects.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <(y position) < [-170]> then
    broadcast [game over v]
  end
end
```


### Next choices

Now choose whether falling ends the game or sends the player back to the start.

- Go to [End the game when the player touches danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/31)
- Go to [Reset the player after a fall](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/34)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Make the player fall below the level and check that the `game over` message runs.
