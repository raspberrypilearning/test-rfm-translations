<h2 class="c-project-heading--task">9A - Add Lava/Spikes</h2>

Add lava or spikes that the player must avoid.

### Choose this route if...

You want a clear danger zone that makes the level riskier.

### Build it

Paint a lava pool or spikes, or use a sharp-looking sprite. Put it where the player needs to be careful.

[![Spike hazard sprite](images/spikes.png)](images/spikes.png)

Type your own respawn position into the white inputs if you want the player to reset.

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  if <<touching [Lava v]?> or <touching [Spike v]?>> then
    broadcast [game over v]
    go to x: () y: ()
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Touch the lava or spikes and check that the `game over` message broadcasts or the player resets.
