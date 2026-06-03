<h2 class="c-project-heading--task">4A - Keys</h2>

Add keyboard controls so the **Player** can move left and right.

## Step 1

Select the **Player** sprite in the sprite pane.

## Step 2

Open the **Code** tab.

![The Code tab in Scratch.](images/tab_code.png)

## Step 3

Make a variable called `move speed` for the **Player** sprite.

This variable controls how far the **Player** moves each time the loop runs. You will choose your own speed in the white input.

## Step 4

Add a script that starts when the green flag is clicked and sets the `move speed`.

```blocks3
+when green flag clicked
+set [move speed v] to ()
+forever
+end
```

## Step 5

Inside the `forever` loop, add controls for moving right.

```blocks3
when green flag clicked
set [move speed v] to ()
forever
+  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
+    change x by (move speed)
+  end
end
```

## Step 6

Add controls for moving left. Put these blocks inside the same `forever` loop, below the right movement blocks.

```blocks3
when green flag clicked
set [move speed v] to ()
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    change x by (move speed)
  end
+  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
+    change x by ((0) - (move speed))
+  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and try the left and right controls.

If the **Player** moves too slowly or too quickly, change the number in the `set [move speed v] to ()` block.

