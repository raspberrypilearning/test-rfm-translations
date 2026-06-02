<h2 class="c-project-heading--task">Add lives</h2>

Let the player make a few mistakes before the game ends.

### Choose this route if...

You want the game to feel more forgiving and more like a bigger platformer.

### Count the player lives

Make a `Lives` variable for all sprites. Change the starting number, respawn position, and delay so they match your own game. Change the sprite names in the touching block to match your real danger sprites.

Add this code to the Stage and Player sprite:

```blocks3
when I receive [start game v]
set [Lives v] to [starting lives]

when I receive [start game v]
forever
  if <touching [Enemy v]?> then
    change [Lives v] by (-1)
    go to x: (start x) y: (start y)
    wait (respawn delay) seconds
  end
  if <touching [Spike v]?> then
    change [Lives v] by (-1)
    go to x: (start x) y: (start y)
    wait (respawn delay) seconds
  end
  if <(Lives) = [0]> then
    broadcast [game over v]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Touch danger a few times and check that `Lives` counts down and the game ends only when it reaches `0`.
