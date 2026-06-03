<h2 class="c-project-heading--task">4B - Mouse Move</h2>

Make the `Player` move toward the mouse pointer.

### Starting here?

Add a sprite called `Player`. Keep the level fairly open so the player can follow the pointer smoothly.

### Choose this route if...

You want simple pointer controls for a maze-like or open platformer route.

### Build it

Type your own move amount into the white input.

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  point towards [mouse-pointer v]
  move () steps
end
```

<h2 class="c-project-heading--task">Test</h2>

Move the mouse pointer and check that the `Player` turns and moves toward it.
