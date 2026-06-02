<h2 class="c-project-heading--task">Add sound effects</h2>

Add a few sounds so jumping, collecting, winning, or losing feels more exciting.

### Choose this route if...

You want your game to feel more lively without changing the game rules.

### Add sounds to scripts you already have

Choose sounds from the Scratch sound library, then add them inside the scripts you already built. Use the `+` blocks below as examples of what to add.

Add this code to the the sprite that already has the action, such as Player or Coin:

```blocks3
if <<key [space v] pressed?> and <(on ground) = [1]>> then
+ play sound [boing v] until done
  set [y speed v] to (jump strength)
  set [on ground v] to [0]
end

when I receive [start game v]
show
forever
  if <touching [Player v]?> then
+   play sound [pop v] until done
    change [Score v] by (1)
    hide
  end
end
```

### Works well with

- [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- [Win by collecting enough things](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/25)
- [Add a win screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/37)

### Next choices

Once the game sounds better, add end screens or test whether the sounds happen at the right moments.

- Go to [Add a win screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/37)
- Go to [Add a game-over screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/38)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Play the part of the game you changed and check that the sound effect happens at the right moment.
