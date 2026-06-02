<h2 class="c-project-heading--task">Add a game-over screen</h2>

Show a special backdrop when the player loses.

### Choose this route if...

You want the player to know straight away that the run is over.

### Switch to a game-over backdrop

Create or choose a backdrop for losing, then use that backdrop name in the script below.

[![Scratch backdrop tab](<images/scratch screenshots/backdrop_tab.png>)](<images/scratch screenshots/backdrop_tab.png>)

Add this code to the Stage:

```blocks3
when I receive [game over v]
switch backdrop to [your game-over backdrop v]
stop [all v]
```


<h2 class="c-project-heading--task">Test</h2>

Trigger your lose condition and check that the Stage changes to the game-over backdrop.
