<h2 class="c-project-heading--task">Add a game-over screen</h2>

Show a special backdrop when the player loses.

### Choose this route if...

You want the player to know straight away that the run is over.

### Switch to a game-over backdrop

Create or choose a backdrop called `Game Over`, or use another clear name and change it in the script.

Add this code to the Stage:

```blocks3
when I receive [game over v]
switch backdrop to [Game Over v]
stop [all v]
```


### Next choices

Add a little more feedback, test the whole game, or move on to sharing it.

- Go to [Add visual feedback](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/39)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)
- Go to [Share your game](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/41)

<h2 class="c-project-heading--task">Test</h2>

Trigger your lose condition and check that the Stage changes to the game-over backdrop.
