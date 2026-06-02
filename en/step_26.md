<h2 class="c-project-heading--task">Win by finding a key and unlocking the exit</h2>

Make the player win only after they find the key and then reach the exit.

### Choose this route if...

You want a stronger puzzle feeling where the player needs two linked goals.

### Unlock the exit with the key

This route works best when the key is somewhere interesting and the exit is easy to spot but not usable at first.

Add this code to the Exit sprite:

```blocks3
when I receive [start game v]
forever
  if <touching [Player v]?> then
    if <(has key) = [1]> then
      broadcast [win v]
    else
      say [Find the key first!] for (2) seconds
    end
  end
end
```


### Next choices

Your win route now has two parts. Add danger, make the win more exciting, or test whether the level feels fair.

- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Add a win screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/37)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Touch the exit without the key and check that it stays locked, then collect the key and touch the exit again to win.
