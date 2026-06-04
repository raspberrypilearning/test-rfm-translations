<h2 class="c-project-heading--task">8A - Animate Your Player</h2>

Switch costumes while the `Player` moves so the character feels more alive.

### Choose this route if...

You would like an optional finishing touch that makes movement feel more lively without changing how it works.

### Build it

Open the **Costumes** tab and check that the `Player` has more than one costume.

[![Scratch costume tab](images/costume_tab.png)](images/costume_tab.png)

Add `next costume` blocks to the movement code on the sprite.

Type your own animation delay into the white inputs.

```blocks3
when green flag clicked
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    next costume
    wait () seconds
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    next costume
    wait () seconds
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Move the `Player` and check that the costume changes while it travels.
