<h2 class="c-project-heading--task">Make a single floor</h2>

Create one simple floor so your player has a safe place to stand.

### Choose this route if...

You want the easiest level shape for testing movement and goals.

### Place one floor across the Stage

Paint the `Platform` sprite as a wide rectangle. Stretch it across the bottom of the Stage so the player has room to move.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
show
go to x: (0) y: (-150)
set size to (180)%
```


### Next choices

With a floor in place, you can add movement, keep the level on one screen, or give the player something to collect.

- Go to [Move left and right with gravity and jumps](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/14)
- Go to [Make a fixed one-screen level](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/20)
- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the floor appears where your `Player` can reach it.
