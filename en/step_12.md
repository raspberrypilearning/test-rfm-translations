<h2 class="c-project-heading--task">Make platforms to jump between</h2>

Create several platforms so your player can jump from place to place.

### Choose this route if...

You want a more classic platformer layout with jumps and different heights.

### Build a simple platform pattern

Paint the `Platform` sprite as a small flat shape. Duplicate it and drag the copies to different heights so the player has stepping stones across the level.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
show
go to x: (-100) y: (-40)
set size to (80)%
```


### Next choices

Your level shape is getting more interesting. Next, add movement, make the platforms move, or place goals on them.

- Go to [Move left and right with gravity and jumps](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/14)
- Go to [Add moving platforms](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/18)
- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that your platforms appear where you want the player to jump.
