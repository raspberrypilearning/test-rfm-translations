<h2 class="c-project-heading--task">Choose an animated Scratch sprite</h2>

Choose a Scratch sprite with more than one costume so you can animate your player later.

### Starting here?

You can start here with an empty project. Pick a sprite with at least two costumes and rename it `Player`.

### Choose this route if...

You want your platformer hero to feel lively and you plan to add animation later.

### Set up an animated player

Choose a sprite from the Scratch library that already has more than one costume. Rename it `Player` so later scripts stay easy to follow. Change the size and start position below so they fit your own sprite and level.

[![Scratch sprite library](<images/scratch screenshots/sprite-choose.png>)](<images/scratch screenshots/sprite-choose.png>)

[![Sprite costume list in Scratch](<images/scratch screenshots/list-costume.png>)](<images/scratch screenshots/list-costume.png>)

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
show
set size to (player size)%
go to x: (start x) y: (start y)
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your `Player` appears in the right place and keeps its costumes ready for animation.
