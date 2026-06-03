<h2 class="c-project-heading--task">9D - Add Hazards</h2>

Add a moving or falling hazard that creates a timed danger.

### Choose this route if...

You want danger based on movement or timing rather than only a fixed lava or spike zone.

### Build it

Place the `Hazard` above or beside a risky part of the level. Type your own positions and timing into the white inputs.

Add this code to the Hazard sprite.

```blocks3
when green flag clicked
go to x: () y: ()
forever
  glide () secs to x: () y: ()
  go to x: () y: ()
  wait () seconds
end
```

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  if <touching [Hazard v]?> then
    broadcast [game over v]
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Hazard` moves and broadcasts `game over` on contact.
