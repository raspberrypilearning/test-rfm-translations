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


<h2 class="c-project-heading--task">Test</h2>

Move the player to the exit and check that the `win` message runs.
