<h2 class="c-project-heading--task">5A - Player Jump/Fall (Simple)</h2>

Add a quick jump and fall motion without building a full gravity system.

## Step 1

Select the **Player** sprite in the sprite pane.

## Step 2

Open the **Code** tab.

![The Code tab in Scratch.](images/tab_code.png)

## Step 3

Decide how high and how fast the **Player** should jump.

You will type your own repeat counts and movement amounts into the white inputs. Larger numbers make a higher or faster jump.

## Step 4

Add a script that starts when the green flag is clicked.

```blocks3
+when green flag clicked
```

## Step 5

Add a `forever` loop below the green flag block.

```blocks3
when green flag clicked
+forever
+end
```

## Step 6

Inside the `forever` loop, add an empty `if` block.

```blocks3
when green flag clicked
forever
+  if <> then
+  end
end
```

## Step 7

Add a `key [space v] pressed?` sensing block to the `if` block.

```blocks3
when green flag clicked
forever
+  if <key [space v] pressed?> then
  end
end
```

## Step 8

Inside the space key `if` block, add a repeat loop for moving up.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
+    repeat ()
+    end
  end
end
```

## Step 9

Inside the repeat loop, add a `change y by` block.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
+      change y by ()
    end
  end
end
```

## Step 10

Below the first repeat loop, add a second repeat loop for moving back down.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
+    repeat ()
+    end
  end
end
```

## Step 11

Inside the second repeat loop, add a `change y by` block.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
+      change y by ()
    end
  end
end
```

## Step 12

Add a subtract operator block to the second `change y by` block.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
+      change y by ((0) - ())
    end
  end
end
```

## Step 13

Add a `wait until` block below both repeat loops.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
      change y by ((0) - ())
    end
+    wait until <>
  end
end
```

## Step 14

Add a `not` operator block to the `wait until` block.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
      change y by ((0) - ())
    end
+    wait until <not <>>
  end
end
```

## Step 15

Add a `key [space v] pressed?` sensing block inside the `not` block.

This makes the **Player** wait until the space key is released before another jump can start.

```blocks3
when green flag clicked
forever
  if <key [space v] pressed?> then
    repeat ()
      change y by ()
    end
    repeat ()
      change y by ((0) - ())
    end
+    wait until <not <key [space v] pressed?>>
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and press space.

If the **Player** jumps too high, too low, too quickly, or too slowly, change the numbers in the repeat loops and `change y by` blocks.
