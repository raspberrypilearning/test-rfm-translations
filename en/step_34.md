<h2 class="c-project-heading--task">Reset the player after a fall</h2>

Send the player back to the start after a fall instead of ending the whole game.

### Choose this route if...

You want a gentler lose rule that keeps the game moving.

### Respawn after a fall

Use the starting position from your player route. If you are also using `Lives`, you can take one away here as well.

Add this code to the Player sprite:

```blocks3
when I receive [start game v]
forever
  if <(y position) < [-170]> then
    go to x: (-180) y: (-110)
    set [y speed v] to [0]
  end
end
```

### Works well with

- [Add a fall-off-the-level danger](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/30)
- [Add lives](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/32)
- [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

### Next choices

Your fall rule is kinder now. Add lives, polish the reset, or test whether the whole level feels fair.

- Go to [Add lives](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/32)
- Go to [Animate your player](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/35)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Make the player fall off the level and check that it returns to the start position.
