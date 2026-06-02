<h2 class="c-project-heading--task">Add coins or stars</h2>

Give the player something satisfying to collect as they explore the level.

### Choose this route if...

You want a goal that can be repeated several times around the level.

### Collect an item

Make a `Score` variable for all sprites. Put your `Coin` or `Star` in a place the player can reach.

[![Coin collectible](images/coin.png)](images/coin.png)

[![Star collectible](images/star.png)](images/star.png)

Add this code to the Stage and Coin or Star sprite:

```blocks3
when I receive [start game v]
set [Score v] to [0]

when I receive [start game v]
show
forever
  if <touching [Player v]?> then
    change [Score v] by (1)
    hide
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Touch a collectible and check that it disappears and the `Score` variable goes up.
