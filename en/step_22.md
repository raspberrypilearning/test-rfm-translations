<h2 class="c-project-heading--task">Add a key</h2>

Place a key in the level so the player can unlock something later.

### Choose this route if...

You want one important item instead of lots of small collectibles.

### Pick up a key

Make a `has key` variable for all sprites. Put the `Key` in a place that feels like a reward to reach.

[![Key sprite](images/key.png)](images/key.png)

Add this code to the Stage and Key sprite:

```blocks3
when I receive [start game v]
set [has key v] to [0]

when I receive [start game v]
show
forever
  if <touching [Player v]?> then
    set [has key v] to [1]
    hide
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Touch the key and check that it disappears and `has key` changes to `1`.
