<h2 class="c-project-heading--task">Add a key</h2>

Place a key in the level so the player can unlock something later.

### Choose this route if...

You want one important item instead of lots of small collectibles.

### Pick up a key

Make a `has key` variable for all sprites. Put the `Key` in a place that feels like a reward to reach.

Add this code to the Stage and Key sprite:

```blocks3
when I receive [start game v]
set [has key v] to [0]

when I receive [start game v]
show
forever
  if <touching [Player v]?> then
    set [has key v] to [1]
    hide
  end
end
```

### Works well with

- [Make your player climb ladders](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/16)
- [Add an exit or special place](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/23)
- [Win by finding a key and unlocking the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/26)

### Next choices

You have a key now. Add an exit that can use it, decide how it unlocks the win, or guard it with danger.

- Go to [Add an exit or special place](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/23)
- Go to [Win by finding a key and unlocking the exit](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/26)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Touch the key and check that it disappears and `has key` changes to `1`.
