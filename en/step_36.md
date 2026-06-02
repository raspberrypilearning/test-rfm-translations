<h2 class="c-project-heading--task">Add sound effects</h2>

Add a few sounds so jumping, collecting, winning, or losing feels more exciting.

### Choose this route if...

You want your game to feel more lively without changing the game rules.

### Add sounds to scripts you already have

Choose sounds from the Scratch sound library, then add them inside the scripts you already built. Use the `+` blocks below as examples of what to add, and replace the sound names with your own choices.

[![Scratch sounds tab](<images/scratch screenshots/sounds_tab.png>)](<images/scratch screenshots/sounds_tab.png>)

[![Scratch sound library](<images/scratch screenshots/list-sounds.png>)](<images/scratch screenshots/list-sounds.png>)

`your jump sound` and `your collect sound` below are placeholders. Replace them with the names of sounds you choose.

Add this code to the sprite that already has the action, such as Player or Coin:

```blocks3
if <<key [space v] pressed?> and <(on ground) = [1]>> then
+ play sound [your jump sound v] until done
  set [y speed v] to (jump strength)
  set [on ground v] to [0]
end

when I receive [start game v]
show
forever
  if <touching [Player v]?> then
+   play sound [your collect sound v] until done
    change [Score v] by (1)
    hide
  end
end
```


<h2 class="c-project-heading--task">Test</h2>

Play the part of the game you changed and check that the sound effect happens at the right moment.
