<h2 class="c-project-heading--task">9E - Add Enemies</h2>

Add a simple patrolling enemy that the player must avoid.

### Choose this route if...

You want a classic platformer challenge that moves back and forth.

### Build it

Choose, draw, or upload an enemy. Put it on a platform or floor where the player must time their movement.

[![Enemy sprite example](images/enemy-blob.png)](images/enemy-blob.png)

Type your own patrol positions and timing into the white inputs.

Add this code to the Enemy sprite.

```blocks3
when green flag clicked
go to x: () y: ()
forever
  glide () secs to x: () y: ()
  glide () secs to x: () y: ()
end
```

Add this code to the Player sprite.

```blocks3
when green flag clicked
forever
  if <touching [Enemy v]?> then
    broadcast [game over v]
    go to x: () y: ()
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and check that the `Enemy` patrols and causes `game over` when touched.
