<h2 class="c-project-heading--task">Add moving platforms</h2>

Make one platform move backwards and forwards so the level feels trickier.

### Choose this route if...

You want to make the level harder without changing the whole backdrop or player.

### Move a platform across the Stage

Use one platform copy first. Once it works, you can duplicate it and change the glide values for extra variety.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
go to x: (-140) y: (-40)
forever
  glide (1) secs to x: (120) y: (-40)
  glide (1) secs to x: (-140) y: (-40)
end
```


### Next choices

Your level is more lively now. Add goals, add danger, or decide what happens if the player gets caught.

- Go to [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [End the game when the player touches danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/31)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the platform moves between the two points you chose.
