<h2 class="c-project-heading--task">7B - Exceed Score</h2>

Make the player win after their `Score` goes past a target.

### Starting here?

Make a variable called `Score` for all sprites. Add a `Player` sprite and one collectible sprite such as `Coin`.

### Choose this route if...

You want the player to collect items before the game can be won.

### Build it

Add or choose a collectible sprite. You can use a coin, star, gem, or any small object.

[![Coin collectible](images/coin.png)](images/coin.png)

[![Star collectible](images/star.png)](images/star.png)

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

Add this code to the collectible sprite.

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
