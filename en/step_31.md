<h2 class="c-project-heading--task">End the game when the player touches danger</h2>

Make danger end the game as soon as it touches the player.

### Choose this route if...

You want a clear, strict lose rule that is easy to understand.

### Broadcast game over on contact

Change the sprite names in the script if your danger uses a different name. You can keep one danger check or add more than one.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <touching [Enemy v]?> then
    broadcast [game over v]
  end
  if <touching [Spike v]?> then
    broadcast [game over v]
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Touch a danger sprite and check that the `game over` message runs straight away.
