<h2 class="c-project-heading--task">Add lives</h2>

Let the player make a few mistakes before the game ends.

### Choose this route if...

You want the game to feel more forgiving and more like a bigger platformer.

### Count the player lives

Make a `Lives` variable for all sprites. Change the sprite names in the touching block to match your real danger sprites.

Add this code to the Stage and Player sprite:

```blocks3
when I receive [start game v]
set [Lives v] to [3]

when I receive [start game v]
forever
  if <touching [Enemy v]?> then
    change [Lives v] by (-1)
    go to x: (-180) y: (-110)
    wait (1) seconds
  end
  if <touching [Spike v]?> then
    change [Lives v] by (-1)
    go to x: (-180) y: (-110)
    wait (1) seconds
  end
  if <(Lives) = [0]> then
    broadcast [game over v]
  end
end
```


### Next choices

Now the player has more chances. Add a game-over screen, show hurt feedback, or decide what happens after a fall.

- Go to [Reset the player after a fall](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/34)
- Go to [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- Go to [Add visual feedback](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/39)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Touch danger a few times and check that `Lives` counts down and the game ends only when it reaches `0`.
