<h2 class="c-project-heading--task">Move left and right with gravity and jumps</h2>

Give your `Player` classic platformer controls with left and right movement, gravity, and jumps.

### Choose this route if...

You want the most traditional platformer movement route.

### Add classic platformer controls

Make these variables for the `Player` sprite: `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, and `on ground`. `move speed` controls left and right movement. `jump strength` controls how high the jump is. `gravity` pulls the player back down.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
set [move speed v] to [5]
set [jump strength v] to [12]
set [gravity v] to [-1]
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
  if <(y position) < [-160]> then
    set y to [-160]
    set [y speed v] to [0]
    set [on ground v] to [1]
  end
end
```


### Next choices

Your game is playable now. Add level behaviour, a goal, danger, or jump to testing if you already have enough pieces.

- Go to [Add moving platforms](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/18)
- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Use the arrow keys or WASD and check that the player runs, jumps, and lands on platforms instead of falling through them.
