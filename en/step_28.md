<h2 class="c-project-heading--task">Add a countdown timer</h2>

Add a timer so the player needs to finish before time runs out.

### Choose this route if...

You want pressure without adding another sprite to the level.

### Count down to zero

Make a `Time` variable for all sprites. Choose a starting time that suits your own level.

Add this code to the Stage:

```blocks3
when I receive [start game v]
set [Time v] to [starting time]
repeat until <(Time) = [0]>
  wait (1) seconds
  change [Time v] by (-1)
end
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Time` variable counts down by one every second.
