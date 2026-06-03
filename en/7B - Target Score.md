<h2 class="c-project-heading--task">7B - Target Score</h2>

Make the player win after their `Score` goes past a set value.

### Choose this route if...

You want the player to collect items before the game can be won.

### Build it

Add or choose a collectable sprite. You can use a coin, star, gem, or any small object.

[![Coin collectable](images/coin.png)](images/coin.png)

[![Star collectable](images/star.png)](images/star.png)

Type your target score into the white input.

Add this code to the Stage.

```blocks3
when green flag clicked
set [Score v] to [0]
forever
  if <(Score) > ()> then
    broadcast [win v]
    stop [this script v]
  end
end
```

Add this code to the collectable sprite.

```blocks3
when green flag clicked
show
forever
  if <touching [Player v]?> then
    change [Score v] by (1)
    hide
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Collect enough items and check that `win` broadcasts when `Score` goes past your target.
