<h2 class="c-project-heading--task">Win by collecting enough things</h2>

Make the player win after collecting a target number of coins or stars.

### Choose this route if...

You want the player to explore and collect before the game ends.

### Check the score to win

Choose how many items the player needs, then use that value in the block below.

`target score` below is a value to replace, not a variable name.

Add this code to the Stage:

```blocks3
when I receive [start game v]
forever
  if <(Score) = [target score]> then
    broadcast [win v]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Collect enough items and check that the `win` message runs when the score reaches your target.
