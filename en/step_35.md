<h2 class="c-project-heading--task">Animate your player</h2>

Switch costumes while the player moves so the character feels more alive.

### Choose this route if...

You want the player to look more lively while moving around the level.

### Change costumes while the player moves

If your player only has one costume, duplicate it first and make a small change so the movement looks different. Change the delay below until the animation speed feels right for your own game.

[![Scratch costume tab](<images/scratch screenshots/costume_tab.png>)](<images/scratch screenshots/costume_tab.png>)

`animation delay` below is a value to replace, not a variable name.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    next costume
    wait (animation delay) seconds
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    next costume
    wait (animation delay) seconds
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Move the player and check that the costumes change while it moves.
