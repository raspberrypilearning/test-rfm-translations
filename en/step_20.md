<h2 class="c-project-heading--task">8A - Animate Your Player</h2>

Switch costumes while the `Player` moves so the character feels more alive.

### Starting here?

Add a sprite called `Player` with at least two costumes. Duplicate and edit a costume if you need another one.

### Choose this route if...

You want optional polish that does not change how movement works.

### Build it

Open the **Costumes** tab and check that the `Player` has more than one costume.

[![Scratch costume tab](images/costume_tab.png)](images/costume_tab.png)

Type your own animation delay into the white inputs.

Add this code to the Player sprite.

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
