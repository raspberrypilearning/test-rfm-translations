<h2 class="c-project-heading--task">9C - Add Obstacles</h2>

BECCA EDITING

Add obstacles that block the player or make the route more interesting.

### Choose this route if...

You want barriers, blocks, crates, walls, or other objects that shape the level without ending the game.

### Build it

Place `Obstacle` sprites where they make the path more interesting. Obstacles should change movement, not automatically cause a loss.

Add these blocks inside your Player movement script after a horizontal movement block.

```blocks3
+ if <touching [Obstacle v]?> then
+   change x by ((0) - (move speed))
+ end
```

<h2 class="c-project-heading--task">Test</h2>

Move into an `Obstacle` and check that it blocks or pushes back the player without ending the game.
