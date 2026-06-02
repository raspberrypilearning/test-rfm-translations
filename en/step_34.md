<h2 class="c-project-heading--task">Reset the player after a fall</h2>

Send the player back to the start after a fall instead of ending the whole game.

### Choose this route if...

You want a gentler lose rule that keeps the game moving.

### Respawn after a fall

Use the bottom of the Scratch Stage, `y = -180`, as the fall check. Keep the start position from your own player route. If you are also using `Lives`, you can take one away here as well.

`start x` and `start y` below are values to replace, not variables to create.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <(y position) < [-180]> then
    go to x: (start x) y: (start y)
    set [y speed v] to [0]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Make the player fall off the level and check that it returns to the start position.
