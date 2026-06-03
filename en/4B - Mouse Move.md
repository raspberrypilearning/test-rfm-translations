<h2 class="c-project-heading--task">4B - Mouse Move</h2>

Make the **Player** move toward the mouse pointer.

## Step 1

Select the **Player** sprite in the sprite pane.

## Step 2

Open the **Code** tab.

![The Code tab in Scratch.](images/tab_code.png)

## Step 3

Add a script that starts when the green flag is clicked.

```blocks3
+when green flag clicked
```

## Step 4

Add a `forever` loop below the green flag block.

```blocks3
when green flag clicked
+forever
+end
```

## Step 5

Inside the `forever` loop, make the **Player** sprite point toward the mouse pointer.

```blocks3
when green flag clicked
forever
+  point towards [mouse-pointer v]
end
```

## Step 6

Add the movement block below the pointing block, inside the same `forever` loop.

```blocks3
when green flag clicked
forever
  point towards [mouse-pointer v]
+  move () steps
end
```

## Step 7

Decide how fast the **Player** should move toward the mouse pointer.

Type a move amount into the white input inside the `move` block. A smaller number gives slower movement, and a larger number gives faster movement.

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and move the mouse pointer around the Stage.

If the **Player** is hard to control, change the number in the `move () steps` block.
