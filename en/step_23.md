<h2 class="c-project-heading--task">Add an exit or special place</h2>

Place an exit, door, finish flag, or special place at the end of the level.

### Choose this route if...

You want a clear place for the player to reach at the end of the game.

### Place the finish point

Move the `Exit` to a place that feels like the end of the challenge. You can use a door, a portal, a treasure room, or another obvious finish point.

Add this code to the Exit sprite:

```blocks3
when I receive [start game v]
show
go to x: (190) y: (-110)
```

### Works well with

- [Move left and right with gravity and jumps](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/14)
- [Win by reaching the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/24)
- [Win by finding a key and unlocking the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/26)

### Next choices

Now decide how reaching this place should trigger a win, or protect it with danger first.

- Go to [Win by reaching the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/24)
- Go to [Win by finding a key and unlocking the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/26)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the exit appears where you want the player to finish.
