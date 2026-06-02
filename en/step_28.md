<h2 class="c-project-heading--task">Add a countdown timer</h2>

Add a timer so the player needs to finish before time runs out.

### Choose this route if...

You want pressure without adding another sprite to the level.

### Count down to zero

Make a `Time` variable for all sprites. Start with a short timer so it is easy to test.

Add this code to the Stage:

```blocks3
when I receive [start game v]
set [Time v] to [30]
repeat until <(Time) = [0]>
  wait (1) seconds
  change [Time v] by (-1)
end
```

### Works well with

- [Make your player climb ladders](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/16)
- [End the game when time runs out](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/33)
- [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)

### Next choices

Add another danger, decide what happens when the time ends, or add a game-over screen.

- Go to [Add falling spikes or danger zones](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/29)
- Go to [End the game when time runs out](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/33)
- Go to [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Time` variable counts down by one every second.
