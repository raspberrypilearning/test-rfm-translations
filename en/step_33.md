<h2 class="c-project-heading--task">End the game when time runs out</h2>

Turn the timer into a proper lose rule by ending the game at zero.

### Choose this route if...

You want the timer to be a real danger instead of just a decoration.

### Watch the timer

This route works best on the Stage because the Stage already manages the timer in many projects.

Add this code to the Stage:

```blocks3
when I receive [start game v]
forever
  if <(Time) = [0]> then
    broadcast [game over v]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Wait until the timer reaches zero and check that the `game over` message runs.
