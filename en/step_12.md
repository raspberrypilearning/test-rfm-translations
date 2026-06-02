<h2 class="c-project-heading--task">Make platforms to jump between</h2>

Create several platforms so your player can jump from place to place.

### Choose this route if...

You want a more classic platformer layout with jumps and different heights.

### Build a simple platform pattern

Paint the `Platform` sprite as a small flat shape. Duplicate it and drag the copies to different heights so the player has stepping stones across the level. Change the first platform values below so they fit your own layout.

The words in the white inputs below are placeholders. Do not make variables called `platform x`, `platform y`, or `platform size`; replace them with your own values.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
show
go to x: (platform x) y: (platform y)
set size to (platform size)%
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your platforms appear where you want the player to jump.
