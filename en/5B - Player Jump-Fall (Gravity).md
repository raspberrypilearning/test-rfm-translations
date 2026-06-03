<h2 class="c-project-heading--task">5B - Player Jump/Fall (Gravity)</h2>

Add gravity-based jumping so the **Player** falls and lands on platforms.

## Step 1

Select the **Player** sprite in the sprite pane.

## Step 2

Open the **Code** tab.

![The Code tab in Scratch.](images/tab_code.png)

## Step 3

Make these variables for the **Player** sprite: `y speed`, `gravity`, `jump strength`, and `on ground`.

The `y speed` variable controls vertical movement. The `gravity` variable pulls the **Player** down. The `jump strength` variable pushes the **Player** up. The `on ground` variable checks whether the **Player** is allowed to jump.

## Step 4

Add a script that starts when the green flag is clicked.

```blocks3
+when green flag clicked
```

## Step 5

Add a block to set `gravity` to your own negative number.

```blocks3
when green flag clicked
+set [gravity v] to ()
```

## Step 6

Add a block to set `jump strength` to your own positive number.

```blocks3
when green flag clicked
set [gravity v] to ()
+set [jump strength v] to ()
```

## Step 7

Add a block to set `y speed` to `0`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
+set [y speed v] to (0)
```

## Step 8

Add a block to set `on ground` to `0`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
+set [on ground v] to (0)
```

## Step 9

Add a `forever` loop below the variable setup blocks.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
+forever
+end
```

## Step 10

Inside the `forever` loop, add an empty `if` block for jumping.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
+  if <> then
+  end
end
```

## Step 11

Add an `and` operator block to the jump `if` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
+  if <<> and <>> then
  end
end
```

## Step 12

Add a `key [space v] pressed?` sensing block to the first side of the `and` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
+  if <<key [space v] pressed?> and <>> then
  end
end
```

## Step 13

Add an `on ground = 1` operator block to the second side of the `and` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
+  if <<key [space v] pressed?> and <(on ground) = (1)>> then
  end
end
```

## Step 14

Inside the jump `if` block, add a block to set `y speed` to `jump strength`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
+    set [y speed v] to (jump strength)
  end
end
```

## Step 15

Add a block to set `on ground` to `0` below the `set [y speed v] to (jump strength)` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
+    set [on ground v] to (0)
  end
end
```

## Step 16

Below the jump `if` block, add a block to change `y speed` by `gravity`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
+  change [y speed v] by (gravity)
end
```

## Step 17

Add a block to change the **Player**'s y position by `y speed`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
+  change y by (y speed)
end
```

## Step 18

Below the vertical movement blocks, add an empty `if` block for checking whether the **Player** is falling.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
+  if <> then
+  end
end
```

## Step 19

Add a `y speed < 0` operator block to the falling `if` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
+  if <(y speed) < (0)> then
  end
end
```

## Step 20

Inside the falling `if` block, add an empty `if` block for checking the platform.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
+    if <> then
+    end
  end
end
```

## Step 21

Add a `touching [Platform v]?` sensing block to the platform `if` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
+    if <touching [Platform v]?> then
    end
  end
end
```

## Step 22

Inside the platform `if` block, add a `repeat until` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
+      repeat until <>
+      end
    end
  end
end
```

## Step 23

Add a `not` operator block to the `repeat until` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
+      repeat until <not <>>
      end
    end
  end
end
```

## Step 24

Add a `touching [Platform v]?` sensing block inside the `not` block.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
+      repeat until <not <touching [Platform v]?>>
      end
    end
  end
end
```

## Step 25

Inside the `repeat until` block, add a `change y by` block to move the **Player** out of the platform.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
+        change y by (1)
      end
    end
  end
end
```

## Step 26

Below the `repeat until` block, add a block to stop the fall.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
+      set [y speed v] to (0)
    end
  end
end
```

## Step 27

Add a block to set `on ground` to `1` after the fall has stopped.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to (0)
+      set [on ground v] to (1)
    end
  end
end
```

## Step 28

Below the falling `if` block, add an empty `if` block for checking whether the **Player** has fallen below the Stage.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to (0)
      set [on ground v] to (1)
    end
  end
+  if <> then
+  end
end
```

## Step 29

Add a `y position < -180` operator block to the new `if` block.

The bottom edge of the Stage has a y position of `-180`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to (0)
      set [on ground v] to (1)
    end
  end
+  if <(y position) < (-180)> then
  end
end
```

## Step 30

Inside the bottom edge `if` block, add a `go to x: () y: ()` block. Choose your own respawn position in the white inputs.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to (0)
      set [on ground v] to (1)
    end
  end
  if <(y position) < (-180)> then
+    go to x: () y: ()
  end
end
```

## Step 31

Below the respawn block, add a block to reset `y speed` to `0`.

```blocks3
when green flag clicked
set [gravity v] to ()
set [jump strength v] to ()
set [y speed v] to (0)
set [on ground v] to (0)
forever
  if <<key [space v] pressed?> and <(on ground) = (1)>> then
    set [y speed v] to (jump strength)
    set [on ground v] to (0)
  end
  change [y speed v] by (gravity)
  change y by (y speed)
  if <(y speed) < (0)> then
    if <touching [Platform v]?> then
      repeat until <not <touching [Platform v]?>>
        change y by (1)
      end
      set [y speed v] to (0)
      set [on ground v] to (1)
    end
  end
  if <(y position) < (-180)> then
    go to x: () y: ()
+    set [y speed v] to (0)
  end
end
```

<h2 class="c-project-heading--task">Test</h2>

Click the green flag and press space to jump.

Check that the **Player** falls back down, lands on the **Platform** sprite, and returns to your chosen respawn position if it falls below the Stage.
