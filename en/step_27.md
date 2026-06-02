<h2 class="c-project-heading--task">Add a patrolling enemy</h2>

Make an enemy move across part of the level so the player has something to avoid.

### Choose this route if...

You want a simple danger route that is easy to see and easy to test.

### Move an enemy backwards and forwards

Put the `Enemy` on the floor or on one platform where the player will need to time their movement carefully. Change the positions and timing below so they fit your own level.

[![Enemy sprite example](images/enemy-blob.png)](images/enemy-blob.png)

Type your own positions and timing into the white inputs below.

Add this code to the Enemy sprite:

```blocks3
when I receive [start game v]
go to x: () y: ()
forever
  glide () secs to x: () y: ()
  glide () secs to x: () y: ()
end
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the enemy moves back and forth across the section you planned.
