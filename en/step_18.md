<h2 class="c-project-heading--task">Add moving platforms</h2>

Make one platform move backwards and forwards so the level feels trickier.

### Choose this route if...

You want to make the level harder without changing the whole backdrop or player.

### Move a platform across the Stage

Use one platform copy first. Once it works, you can duplicate it and change the positions and timing for extra variety.

Type your own positions and timing into the white inputs below.

Add this code to the Platform sprite:

```blocks3
when I receive [start game v]
go to x: () y: ()
forever
  glide () secs to x: () y: ()
  glide () secs to x: () y: ()
end
```


<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the platform moves between the two points you chose.
