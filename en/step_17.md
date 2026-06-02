<h2 class="c-project-heading--task">Make your player follow the mouse</h2>

Make the `Player` point at the mouse pointer and follow it around the Stage.

### Choose this route if...

You want a very simple control route that feels good for a maze or collection game.

### Follow the pointer

Keep the level fairly open so the player can follow the mouse smoothly.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  point towards [mouse-pointer v]
  move (4) steps
end
```


### Next choices

With controls in place, you can add an exit, add danger, or keep the level bounded.

- Go to [Add walls or boundaries](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/13)
- Go to [Add an exit or special place](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/23)
- Go to [Add falling spikes or danger zones](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/29)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Move the mouse and check that the player turns and follows the pointer.
