<h2 class="c-project-heading--task">Make a scrolling level</h2>

Make level pieces slide past the player so the game feels wider than one screen.

### Choose this route if...

You want a level that feels larger than one Stage without making the player tiny.

### Scroll the level pieces

Add the script below to each level sprite except `Player`. Use it on `Platform`, `Coin`, `Enemy`, and `Exit` if you want them all to scroll together.

Add this code to the level sprite such as Platform, Coin, Exit, or Enemy:

```blocks3
when I receive [start game v]
forever
  if <<(x position of [Player v]) > [40]> and <key [right arrow v] pressed?>> then
    change x by (-5)
  end
  if <<(x position of [Player v]) < [-40]> and <key [left arrow v] pressed?>> then
    change x by (5)
  end
end
```

### Works well with

- [Add walls or boundaries](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/13)
- [Move left and right with gravity and jumps](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/14)
- [Add an exit or special place](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/23)

### Next choices

Once the level scrolls, add a goal, add danger, or test whether the whole route still feels fair.

- Go to [Add an exit or special place](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/23)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Move the player left and right and check that the level pieces scroll past instead of all staying still.
