<h2 class="c-project-heading--task">Add a patrolling enemy</h2>

Make an enemy move across part of the level so the player has something to avoid.

### Choose this route if...

You want a simple danger route that is easy to see and easy to test.

### Move an enemy backwards and forwards

Put the `Enemy` on the floor or on one platform where the player will need to time their movement carefully.

Add this code to the Enemy sprite:

```blocks3
when I receive [start game v]
go to x: (-120) y: (-96)
forever
  glide (1) secs to x: (100) y: (-96)
  glide (1) secs to x: (-120) y: (-96)
end
```


### Next choices

Add another kind of danger, or choose what happens when the player gets caught.

- Go to [Add a countdown timer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/28)
- Go to [End the game when the player touches danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/31)
- Go to [Add lives](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/32)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the enemy moves back and forth across the section you planned.
