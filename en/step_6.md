<h2 class="c-project-heading--task">Choose a static Scratch sprite</h2>

Pick a simple Scratch sprite and turn it into your `Player`.

### Starting here?

You can begin here even if you skipped the world routes. Add one sprite and rename it `Player`.

### Choose this route if...

You want a quick player so you can focus on movement and level design.

### Set up your player sprite

Choose a sprite from the Scratch library and rename it `Player`. A clear full-body sprite is easiest to control and see. Change the size and start position below so they fit your own sprite and level.

[![Scratch sprite library](<images/scratch screenshots/sprite-choose.png>)](<images/scratch screenshots/sprite-choose.png>)

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
show
set size to (player size)%
go to x: (start x) y: (start y)
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your `Player` appears in the same starting place each time.
