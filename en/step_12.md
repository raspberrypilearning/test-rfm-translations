<h2 class="c-project-heading--task">5A - Player Jump/Fall (Simple)</h2>

Add a quick jump and fall motion without building a full gravity system.

### Starting here?

Add a sprite called `Player` and a simple floor called `Platform` before you test the jump.

### Choose this route if...

You want an easy jump that works quickly in a small game.

### Build it

Type your own repeat counts and jump amounts into the white inputs below.

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
      change y by ((0) - ())
    end
    wait until <not <key [space v] pressed?>>
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Press space and check that the `Player` moves up and then comes back down.
