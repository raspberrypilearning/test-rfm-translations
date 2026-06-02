<h2 class="c-project-heading--task">Move left and right with jump but no gravity</h2>

Give your `Player` simple left and right movement with a quick jump arc.

### Choose this route if...

You want a simple movement route that still feels like a platform game.

### Add simple running and jumping

This route works best on a flat floor or a very small number of platforms. Make a `move speed` variable for the `Player` sprite, then change the values below until they suit your own player and level.

Type your own values into the white inputs below.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
set [move speed v] to ()
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    change x by (move speed)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    change x by ((0) - (move speed))
  end
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
      change y by ((0) - ())
    end
    wait until <not <key [space v] pressed?>>
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Use the controls and check that the player moves left and right and makes a quick jump when you press space.
