<h2 class="c-project-heading--task">Move left and right with jump but no gravity</h2>

Give your `Player` simple left and right movement with a quick jump arc.

### Choose this route if...

You want a simple movement route that still feels like a platform game.

### Add simple running and jumping

This route works best on a flat floor or a very small number of platforms.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
set [move speed v] to [6]
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    change x by (move speed)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    change x by ((0) - (move speed))
  end
  if <key [space v] pressed?> then
    repeat (8)
      change y by (6)
    end
    repeat (8)
      change y by (-6)
    end
    wait until <not <key [space v] pressed?>>
  end
end
```

### Works well with

- [Make a single floor](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/11)
- [Make a fixed one-screen level](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/20)
- [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)

### Next choices

You have a lighter movement route now. Choose a goal, add danger, or keep the whole level on one screen.

- Go to [Make a fixed one-screen level](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/20)
- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Use the controls and check that the player moves left and right and makes a quick jump when you press space.
