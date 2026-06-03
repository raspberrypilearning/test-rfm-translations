<h2 class="c-project-heading--task">4A - Keys</h2>

Add keyboard controls so the `Player` can move left and right.

### Starting here?

Add a sprite called `Player`. Keyboard controls work best on a laptop or desktop with a physical keyboard.

### Choose this route if...

You want classic platformer controls with arrow keys, and optional WASD keys.

### Build it

Make a variable called `move speed` for the `Player` sprite. Type your own speed into the white input.

Add this code to the Player sprite.

```blocks3
when green flag clicked
set [move speed v] to ()
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    change x by (move speed)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    change x by ((0) - (move speed))
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Press the left and right controls and check that the `Player` moves across the Stage.
