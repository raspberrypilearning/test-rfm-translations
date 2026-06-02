<h2 class="c-project-heading--task">Add visual feedback</h2>

Add a visible reaction when the player wins, gets hurt, or collects something.

### Choose this route if...

You want the game to feel clearer without changing its main rules.

### Show a reaction on screen

Use one small effect at first. A size change, colour effect, or short flashing animation is enough.

Add this code to the Player sprite:

```blocks3
when I receive [win v]
repeat (6)
  change size by (10)
  wait (0.1) seconds
  change size by (-10)
  wait (0.1) seconds
end

when I receive [game over v]
change [ghost v] effect by (40)
```

### Works well with

- [Add coins or stars](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/21)
- [Add lives](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/32)
- [Animate your player](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/35)

### Next choices

Your game now reacts more clearly. Test the whole route, or get ready to share it.

- Go to [Animate your player](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/35)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)
- Go to [Share your game](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/41)

<h2 class="c-project-heading--task">Test</h2>

Trigger the event you changed and check that the player or another sprite shows a clear visual reaction.
