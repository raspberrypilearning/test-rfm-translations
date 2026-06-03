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

```blocks3
+when green flag clicked
```

## Step 5

Add a block to set the rotation style to **left-right** so the **Player** does not turn upside down.

```blocks3
when green flag clicked
+set rotation style [left-right v]
```

## Step 6

Add a block to set the `move speed`.

```blocks3
when green flag clicked
set rotation style [left-right v]
+set [move speed v] to ()
```

## Step 7

Add a block to make the **Player** start by facing right.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
+point in direction (90)
```

## Step 8

Add a `forever` loop below the direction block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
+forever
+end
```

## Step 9

Inside the `forever` loop, add an empty `if` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
+  if <> then
+  end
end
```

## Step 10

Add an `or` operator block to the `if` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
+  if <<> or <>> then
  end
end
```

## Step 11

Add a `key [right arrow v] pressed?` sensing block to the first side of the `or` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
+  if <<key [right arrow v] pressed?> or <>> then
  end
end
```

## Step 12

Add a `key [d v] pressed?` sensing block to the second side of the `or` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
+  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
  end
end
```

## Step 13

Inside the right direction `if` block, add a block to point right.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
+    point in direction (90)
  end
end
```

## Step 14

Below the right direction `if` block, add another empty `if` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
+  if <> then
+  end
end
```

## Step 15

Add an `or` operator block to the new `if` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
+  if <<> or <>> then
  end
end
```

## Step 16

Add a `key [left arrow v] pressed?` sensing block to the first side of the `or` block.

```blocks3
when green flag clicked
set rotation style [left-right v]
set [move speed v] to ()
point in direction (90)
forever
  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
    point in direction (90)
  end
+  if <<key [left arrow v] pressed?> or <>> then
  end
end
```

## Step 17

Add a `key [a v] pressed?` sensing block to the second side of the `or` block.

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
  end
end
```

## Step 18

Inside the left direction `if` block, add a block to point left.

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
+    point in direction (-90)
  end
end
```

## Step 19

Add a `move` block below both direction checks, inside the same `forever` loop.

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
+  move () steps
end
```

## Step 20

Add the `move speed` variable block to the `move` block.

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

## Step 21

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
