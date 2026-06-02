<h2 class="c-project-heading--task">Use an example generated sprite</h2>

Use one of the example PNG sprites if you want a ready-made player image.

### Starting here?

You can start here with an empty project.

### Choose this route if...

You want a player quickly but you would like something more custom than a Scratch library sprite.

### Upload one of the example player sprites

Choose **Upload Sprite** and select one of these example player sprites. Rename the sprite `Player` if Scratch does not do that for you. Change the size and start position below so they fit your own sprite and level.

[![Player robot sprite](images/example-sprite-player-robot.png)](images/example-sprite-player-robot.png)

[![Player creature sprite](images/example-sprite-player-creature.png)](images/example-sprite-player-creature.png)

[![Player adventurer sprite](images/example-sprite-player-adventurer.png)](images/example-sprite-player-adventurer.png)

The words in the white inputs below are placeholders. Do not make variables called `player size`, `start x`, or `start y`; replace them with your own values.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
show
set size to (player size)%
go to x: (start x) y: (start y)
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your example `Player` sprite appears in the correct place.
