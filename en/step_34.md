<h2 class="c-project-heading--task">Reset the player after a fall</h2>

Send the player back to the start after a fall instead of ending the whole game.

### Choose this route if...

You want a gentler lose rule that keeps the game moving.

### Respawn after a fall

Use the fall position and starting position from your own player route. If you are also using `Lives`, you can take one away here as well.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <(y position) < [fall y]> then
    go to x: (start x) y: (start y)
    set [y speed v] to [0]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Make the player fall off the level and check that it returns to the start position.
