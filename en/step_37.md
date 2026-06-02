<h2 class="c-project-heading--task">Add a win screen</h2>

Show a special backdrop when the player wins.

### Choose this route if...

You want the ending to feel more obvious and more rewarding.

### Switch to a win backdrop

Create or choose a backdrop called `You Win`, or use another clear name and change it in the script.

Add this code to the Stage:

```blocks3
when I receive [win v]
switch backdrop to [You Win v]
stop [all v]
```


### Next choices

Your victory now has a clear ending. Add a matching game-over screen, test the whole game, or get ready to share it.

- Go to [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)
- Go to [Share your game](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/41)

<h2 class="c-project-heading--task">Test</h2>

Trigger your win condition and check that the Stage changes to the win backdrop.
