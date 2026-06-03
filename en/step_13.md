<h2 class="c-project-heading--task">5B - Player Jump/Fall (Gravity)</h2>

Add gravity-based jumping so the `Player` falls and lands on platforms.

### Starting here?

Add a sprite called `Player` and a rectangle sprite called `Platform` before you begin.

### Choose this route if...

You want a more classic platformer feel with gravity, falling, and stronger jumps.

### Build it

Make these variables for the `Player` sprite: `y speed`, `gravity`, `jump strength`, and `on ground`. Type your own starting values and respawn position into the white inputs.

Add this code to the Player sprite.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to [0]
set [on ground v] to [0]
forever
  if <<key [space v] pressed?> and <(on ground) = [1]>> then
    set [y speed v] to (jump strength)
    set [on ground v] to [0]
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < [0]> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to [0]
      set [on ground v] to [1]
    end
  end
  if <(y position) < [-180]> then
    go to x: () y: ()
    set [y speed v] to [0]
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Jump and check that the `Player` falls back down and can land on the `Platform` sprite.
