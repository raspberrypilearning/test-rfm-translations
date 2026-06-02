<h2 class="c-project-heading--task">Add falling spikes or danger zones</h2>

Add a spike hazard or falling danger so the player has a risky area to avoid.

### Choose this route if...

You want a visible danger that feels different from an enemy.

### Drop a hazard into the level

You can keep the spikes still as a danger zone, or use the code below to make them fall and reset.

Add this code to the Spike sprite:

```blocks3
when I receive [start game v]
show
go to x: (120) y: (160)
forever
  glide (1) secs to x: (120) y: (-100)
  go to x: (120) y: (160)
  wait (1) seconds
end
```

### Works well with

- [Move left and right with gravity and jumps](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/14)
- [End the game when the player touches danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/31)
- [Reset the player after a fall](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/34)

### Next choices

Add another danger, or choose what happens when the player touches or falls into it.

- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [End the game when the player touches danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/31)
- Go to [Reset the player after a fall](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/34)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the spikes appear where you expect and behave like a hazard.
