<h2 class="c-project-heading--task">8B - Make Your Player Sprint</h2>

Add a sprint control so the `Player` can move faster when a key is pressed.

### Choose this route if...

You want an optional speed boost for longer jumps, harder levels, or timed challenges.

### Build it

Make variables called `move speed` and `sprint speed` for the `Player` sprite. 

Add the variables to the Player sprite.

Type your own speeds into the white inputs.

Add a condition to check whether the `shift` key is pressed so it can act as the sprint control key.

Use the variable values to control how far the player's coordinates change.

```blocks3
when green flag clicked
set [move speed v] to ()
set [sprint speed v] to ()
forever
  if <key [shift v] pressed?> then
    if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
      change x by (sprint speed)
    end
    if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
      change x by ((0) - (sprint speed))
    end
  else
    if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
      change x by (move speed)
    end
    if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
      change x by ((0) - (move speed))
    end
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Hold shift while moving and check that the `Player` travels faster.
