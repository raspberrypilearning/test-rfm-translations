<h2 class="c-project-heading--task">Add an exit or special place</h2>

Place an exit, door, finish flag, or special place at the end of the level.

### Choose this route if...

You want a clear place for the player to reach at the end of the game.

### Place the finish point

Move the `Exit` to a place that feels like the end of the challenge. You can use a door, a portal, a treasure room, or another obvious finish point. Change the position below so it fits your own level.

[![Exit door sprite](images/exit-door.png)](images/exit-door.png)

Type the exit position into the white inputs below.

Add this code to the Exit sprite:

```blocks3
when I receive [start game v]
show
go to x: () y: ()
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the exit appears where you want the player to finish.
