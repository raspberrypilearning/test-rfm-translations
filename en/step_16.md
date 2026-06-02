<h2 class="c-project-heading--task">Make your player climb ladders</h2>

Let your `Player` run, jump, and climb ladders like a classic platform game.

### Choose this route if...

You want a more old-school platformer route with vertical climbing.

### Add ladder climbing movement

Draw the `Ladder` sprite as a tall shape that the player can touch. Make these variables for the `Player` sprite: `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, and `on ground`.

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
  if <touching [Ladder v]?> then
    set [y speed v] to [0]
    if <<key [up arrow v] pressed?> or <key [w v] pressed?>> then
      change y by (move speed)
    end
    if <<key [down arrow v] pressed?> or <key [s v] pressed?>> then
      change y by ((0) - (move speed))
    end
  else
    if <<key [space v] pressed?> and <(on ground) = [1]>> then
      set [y speed v] to (jump strength)
      set [on ground v] to [0]
    end
    change [y speed v] by (gravity)
    change y by (y speed)
  end
  if <(y speed) < [0]> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to [0]
      set [on ground v] to [1]
    end
  end
end
```


### Next choices

Now that the player can climb, keep the level in bounds, add a goal, or add time pressure.

- Go to [Add walls or boundaries](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/13)
- Go to [Add a key](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/22)
- Go to [Add a countdown timer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/28)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Use the keyboard and check that the player can run, jump, and climb up and down the ladder.
