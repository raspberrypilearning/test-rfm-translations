<h2 class="c-project-heading--task">Make a single floor</h2>

Create one simple floor so your player has a safe place to stand.

### Choose this route if...

You want the easiest level shape for testing movement and goals.

### Place one floor across the Stage

Paint the `Platform` sprite as a wide rectangle. Stretch it across the bottom of the Stage so the player has room to move. Change the position and size below so the floor fits your own level.

Type your own floor position and size into the white inputs below.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
show
go to x: () y: ()
set size to (floor size)%
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the floor appears where your `Player` can reach it.
