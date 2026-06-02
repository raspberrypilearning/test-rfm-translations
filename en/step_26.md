<h2 class="c-project-heading--task">Win by finding a key and unlocking the exit</h2>

Make the player win only after they find the key and then reach the exit.

### Choose this route if...

You want a stronger puzzle feeling where the player needs two linked goals.

### Unlock the exit with the key

This route works best when the key is somewhere interesting and the exit is easy to spot but not usable at first. Change the message below if you want different words in your own game.

Type your locked message into the white input below.

Add this code to the Exit sprite:

```blocks3
when I receive [start game v]
forever
  if <touching [Player v]?> then
    if <(has key) = [1]> then
      broadcast [win v]
    else
      say [] for (2) seconds
    end
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Touch the exit without the key and check that it stays locked, then collect the key and touch the exit again to win.
