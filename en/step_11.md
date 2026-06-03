<h2 class="c-project-heading--task">4C - Always Moving</h2>

Make the `Player` keep moving while the learner controls its direction.

### Starting here?

Add a sprite called `Player`. This route works best when the level has enough empty space to move around.

### Choose this route if...

You want an auto-runner or always-moving challenge where the player must steer quickly.

### Build it

Make a variable called `move speed` for the `Player` sprite. Type your own speed into the white input.

Add this code to the Player sprite.

```blocks3
when green flag clicked
set [move speed v] to ()
forever
  if <key [up arrow v] pressed?> then
    point in direction (0)
  end
  if <key [right arrow v] pressed?> then
    point in direction (90)
  end
  if <key [down arrow v] pressed?> then
    point in direction (180)
  end
  if <key [left arrow v] pressed?> then
    point in direction (-90)
  end
  move (move speed) steps
  if on edge, bounce
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Player` keeps moving while the arrow keys change direction.
