<h2 class="c-project-heading--task">End the game when time runs out</h2>

Turn the timer into a proper lose rule by ending the game at zero.

### Choose this route if...

You want the timer to be a real danger instead of just a decoration.

### Watch the timer

This route works best on the Stage because the Stage already manages the timer in many projects.

Add this code to the Stage:

```blocks3
when I receive [start game v]
forever
  if <(Time) = [0]> then
    broadcast [game over v]
  end
end
```

### Works well with

- [Add a countdown timer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/28)
- [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

### Next choices

Now the timer can beat the player. Add a game-over screen, test the game, or get ready to share it.

- Go to [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)
- Go to [Share your game](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/41)

<h2 class="c-project-heading--task">Test</h2>

Wait until the timer reaches zero and check that the `game over` message runs.
