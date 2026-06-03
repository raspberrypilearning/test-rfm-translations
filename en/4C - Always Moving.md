<h2 class="c-project-heading--task">4C - Always Moving</h2>

Make the `Player` keep moving left and right while the learner controls its horizontal direction.

### Choose this route if...

You want an auto-runner or always-moving challenge where the player must switch direction quickly.

### Build it

Make a variable called `move speed` for the `Player` sprite. Type your own speed into the white input.

Add this code to the Player sprite.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    point in direction (-90)
  end
  move (move speed) steps
  if on edge, bounce
  end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Player` keeps moving left and right while the controls change direction.
