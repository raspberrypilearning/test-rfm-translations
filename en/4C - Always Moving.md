<h2 class="c-project-heading--task">4C - Always Moving</h2>

Make the **Player** keep moving left and right while the learner controls its horizontal direction.

## Step 1

Select the **Player** sprite in the sprite pane.

## Step 2

Open the **Code** tab.

![The Code tab in Scratch.](images/tab_code.png)

## Step 3

Make a variable called `move speed` for the **Player** sprite.

This variable controls how far the **Player** moves each time the loop runs. You will choose your own speed in the white input.

## Step 4

Add a script that starts when the green flag is clicked.

Set the rotation style to **left-right** so the **Player** does not turn upside down. Then set the `move speed` and make the **Player** start by facing right.

```blocks3
+when green flag clicked
+set rotation style [left-right v]
+set [move speed v] to ()
+point in direction (90)
+forever
+end
```

## Step 5

Inside the `forever` loop, add controls that change the direction to the right.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
+  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
+    point in direction (90)
+  end
end
```

## Step 6

Add controls that change the direction to the left. Put these blocks inside the same `forever` loop.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
+  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
+    point in direction (-90)
+  end
end
```

## Step 7

Add the movement block below the direction controls, inside the same `forever` loop.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    point in direction (-90)
  end
+  move (move speed) steps
end
```

## Step 8

Add the edge bounce block below the movement block so the **Player** stays on the Stage.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
    point in direction (-90)
  end
  move (move speed) steps
+  if on edge, bounce
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and use the left and right controls to switch direction.

If the **Player** moves too slowly or too quickly, change the number in the `set [move speed v] to ()` block.
