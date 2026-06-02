<h2 class="c-project-heading--task">Start another level</h2>

Use a new backdrop or layout so the player can continue into a second level.

### Choose this route if...

You want to turn one platformer challenge into a bigger adventure.

### Move on to level two

Make a second backdrop or a new set of platforms first. Then change your first win route so it broadcasts `next level` instead of `win` when the first level is finished.

Add this code to the Stage:

```blocks3
when I receive [next level v]
switch backdrop to [Level 2 v]
broadcast [start game v]
```

### Works well with

- [Add moving platforms](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/18)
- [Win by reaching the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/24)
- [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)

### Next choices

A new level lets you loop back through the project: pick a new world, new platforms, new goals, or new dangers.

- Go to [Choose a Scratch backdrop](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/2)
- Go to [Make platforms to jump between](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/12)
- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)

<h2 class="c-project-heading--task">Test</h2>

Trigger the `next level` message and check that the Stage switches to the new level and starts it.
