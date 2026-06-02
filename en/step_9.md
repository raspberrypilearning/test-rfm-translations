<h2 class="c-project-heading--task">Upload a sprite</h2>

Upload a player image from your device and use it as your `Player` sprite.

### Starting here?

You can start here with an empty project. Choose **Upload Sprite** and rename the new sprite `Player`.

### Choose this route if...

You already have an image you want to use for the main character.

### Use your own player image

Choose an image that is easy to see at a small size. Change the size and start position below so they fit your own sprite and level.

The words in the white inputs below are placeholders. Do not make variables called `player size`, `start x`, or `start y`; replace them with your own values.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
show
set size to (player size)%
go to x: (start x) y: (start y)
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your uploaded `Player` appears at the starting point.
