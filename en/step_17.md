<h2 class="c-project-heading--task">Make your player follow the mouse</h2>

Make the `Player` point at the mouse pointer and follow it around the Stage.

### Choose this route if...

You want a very simple control route that feels good for a maze or collection game.

### Follow the pointer

Keep the level fairly open so the player can follow the mouse smoothly. Change the move amount below until it feels right for your own game.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  point towards [mouse-pointer v]
  move (your speed) steps
end
```


<h2 class="c-project-heading--task">Test</h2>

Move the mouse and check that the player turns and follows the pointer.
