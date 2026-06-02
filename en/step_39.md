<h2 class="c-project-heading--task">Add visual feedback</h2>

Add a visible reaction when the player wins, gets hurt, or collects something.

### Choose this route if...

You want the game to feel clearer without changing its main rules.

### Show a reaction on screen

Use one small effect at first. A size change, colour effect, or short flashing animation is enough. Change the values below so the effect fits your own sprite and style.

Type your own effect values into the white inputs below.

Add this code to the Player sprite:

```blocks3
when I receive [win v]
repeat ()
  change size by ()
  wait () seconds
  change size by ((0) - ())
  wait () seconds
end

when I receive [game over v]
change [ghost v] effect by ()
```


<h2 class="c-project-heading--task">Test</h2>

Trigger the event you changed and check that the player or another sprite shows a clear visual reaction.
