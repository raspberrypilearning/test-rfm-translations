<h2 class="c-project-heading--task">7A - Get to Exit Sprite (Default)</h2>

Make the player win when they touch the `Exit` sprite.

### Choose this route if...

You want the simplest win condition for a platformer level.

### Build it

Use `broadcast [win v]` so other routes can react to winning later.

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  if <touching [Exit v]?> then
    broadcast [win v]
    stop [this script v]
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Move the `Player` to the `Exit` and check that the win message appears.
