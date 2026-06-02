<h2 class="c-project-heading--task">Win by reaching the exit</h2>

Make the player win as soon as they reach the exit.

### Choose this route if...

You want the clearest and fastest win condition.

### Trigger a win at the exit

This route works well when the player already has movement and a clear finish point.

Add this code to the Exit sprite:

```blocks3
when I receive [start game v]
forever
  if <touching [Player v]?> then
    broadcast [win v]
  end
end
```


### Next choices

Your game can be won now. Add danger, polish the result, or test the whole route from start to finish.

- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Animate your player](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/35)
- Go to [Add a win screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/37)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Move the player to the exit and check that the `win` message runs.
