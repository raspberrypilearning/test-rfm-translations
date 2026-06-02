<h2 class="c-project-heading--task">Win by collecting enough things</h2>

Make the player win after collecting a target number of coins or stars.

### Choose this route if...

You want the player to explore and collect before the game ends.

### Check the score to win

Choose how many items the player needs. Start with a small number such as `3` or `5` so it is easy to test.

Add this code to the Stage:

```blocks3
when I receive [start game v]
forever
  if <(Score) = [5]> then
    broadcast [win v]
  end
end
```


### Next choices

Now the player has a collection goal. Add danger, reward the win, or test the whole game.

- Go to [Add a patrolling enemy](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/27)
- Go to [Add sound effects](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/36)
- Go to [Add a win screen](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/37)
- Go to [Test and debug your platformer](https://projects.raspberrypi.org/en/projects/branching-pathways-platformer/40)

<h2 class="c-project-heading--task">Test</h2>

Collect enough items and check that the `win` message runs when the score reaches your target.
