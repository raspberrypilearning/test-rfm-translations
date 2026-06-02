<h2 class="c-project-heading--task">Make a scrolling level</h2>

Make level pieces slide past the player so the game feels wider than one screen.

### Choose this route if...

You want a level that feels larger than one Stage without making the player tiny.

### Scroll the level pieces

Add the script below to each level sprite except `Player`. Use it on `Platform`, `Coin`, `Enemy`, and `Exit` if you want them all to scroll together. Change the scroll points and speed so they fit your own level.

Add this code to the level sprite such as Platform, Coin, Exit, or Enemy:

```blocks3
when I receive [start game v]
forever
  if <<(x position of [Player v]) > [right scroll point]> and <key [right arrow v] pressed?>> then
    change x by ((0) - (scroll speed))
  end
  if <<(x position of [Player v]) < [left scroll point]> and <key [left arrow v] pressed?>> then
    change x by (scroll speed)
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Move the player left and right and check that the level pieces scroll past instead of all staying still.
