<h2 class="c-project-heading--task">Move left and right with gravity and jumps</h2>

Give your `Player` classic platformer controls with left and right movement, gravity, and jumps.

### Choose this route if...

You want the most traditional platformer movement route.

### Add classic platformer controls

Make these variables for the `Player` sprite: `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, and `on ground`. `move speed` controls left and right movement. `jump strength` controls how high the jump is. `gravity` pulls the player back down. Change the tuning values and floor position below so they fit your own level.

Make the variables listed above. In the setup block, `your move speed`, `your jump strength`, `your gravity`, and `floor y` are placeholder values, not extra variables.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
set [move speed v] to [your move speed]
set [jump strength v] to [your jump strength]
set [gravity v] to [your gravity]
set [x speed v] to [0]
set [y speed v] to [0]
set [on ground v] to [0]
forever
  set [x speed v] to [0]
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    set [x speed v] to (move speed)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    set [x speed v] to ((0) - (move speed))
  end
  change x by (x speed)
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
  if <(y position) < [floor y]> then
    set y to [floor y]
    set [y speed v] to [0]
    set [on ground v] to [1]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Use the arrow keys or WASD and check that the player runs, jumps, and lands on platforms instead of falling through them.
