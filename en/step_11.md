## 4C - Always Moving

Make the **Player** keep moving, and use the arrow keys to change direction.

## Step 1

> [!TASK]
>
> Select the **Player** sprite in the sprite pane.

## Step 2

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

## Step 3

> [!TASK]
>
> The starter project already includes the `move vertically` block, the **Player** setup script, and these **Player** variables:
>
> `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, `on ground`, `vertical steps`
>
> If you can already see them in your starter project, just check this step off.

## Step 4

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> Inside a `forever`{:class="block3control"} loop, set `x speed`{:class="block3variables"} to `move speed` if `x speed` is `0`.
>
> ```blocks3
> +when green flag clicked
> +forever
> +  if <(x speed) = (0)> then
> +    set [x speed v] to (move speed)
> +  end
> +end
> ```

## Step 5

> [!TASK]
>
> Add an `if`{:class="block3control"} block for turning right.
>
> If the `right arrow` key is pressed, set `x speed`{:class="block3variables"} to `move speed` and point the **Player** right.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
> +  if <key [right arrow v] pressed?> then
> +    set [x speed v] to (move speed)
> +    point in direction (90)
> +  end
> end
> ```

## Step 6

> [!TASK]
>
> Add another `if`{:class="block3control"} block for turning left.
>
> If the `left arrow` key is pressed, set `x speed`{:class="block3variables"} to `0 - move speed` and point the **Player** left.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
>   if <key [right arrow v] pressed?> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
> +  if <key [left arrow v] pressed?> then
> +    set [x speed v] to ((0) - (move speed))
> +    point in direction (-90)
> +  end
> end
> ```

## Step 7

> [!TASK]
>
> At the bottom of the `forever`{:class="block3control"} loop, add `change x by (x speed)`{:class="block3motion"}.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
>   if <key [right arrow v] pressed?> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
>   if <key [left arrow v] pressed?> then
>     set [x speed v] to ((0) - (move speed))
>     point in direction (-90)
>   end
>
> +  change x by (x speed)
> end
> ```

## Step 8

> [!TASK]
>
> Above `change x by (x speed)`{:class="block3motion"}, add an `if`{:class="block3control"} block that checks whether the `space` key is pressed.
>
> Inside the `if`{:class="block3control"} block, set `y speed`{:class="block3variables"} to `jump strength`{:class="block3variables"}.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
>   if <key [right arrow v] pressed?> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
>   if <key [left arrow v] pressed?> then
>     set [x speed v] to ((0) - (move speed))
>     point in direction (-90)
>   end
>
> +  if <key [space v] pressed?> then
> +    set [y speed v] to (jump strength)
> +  end
>
>   change x by (x speed)
> end
> ```

## Step 9

> [!TASK]
>
> At the bottom of the `forever`{:class="block3control"} loop, add the `move vertically` block from **My Blocks**.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
>   if <key [right arrow v] pressed?> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
>   if <key [left arrow v] pressed?> then
>     set [x speed v] to ((0) - (move speed))
>     point in direction (-90)
>   end
>
>   if <key [space v] pressed?> then
>     set [y speed v] to (jump strength)
>   end
>
>   change x by (x speed)
> +  move vertically
> end
> ```

## Step 10

> [!TASK]
>
> Click the green flag and test your controls.
>
> Press `space` to jump, then press `space` again while the **Player** is still in the air.
>
> You should see that the **Player** can jump again before landing. This is called a double jump.

## Step 11

> [!TASK]
>
> To stop the double jump, add an `and`{:class="block3operators"} condition to the space key `if`{:class="block3control"} block.
>
> The **Player** should only jump if the `space` key is pressed and `on ground`{:class="block3variables"} is `1`.
>
> ```blocks3
> when green flag clicked
> forever
>   if <(x speed) = (0)> then
>     set [x speed v] to (move speed)
>   end
>
>   if <key [right arrow v] pressed?> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
>   if <key [left arrow v] pressed?> then
>     set [x speed v] to ((0) - (move speed))
>     point in direction (-90)
>   end
>
> -  if <key [space v] pressed?> then
> +  if <<key [space v] pressed?> and <(on ground) = (1)>> then
>     set [y speed v] to (jump strength)
>   end
>
>   change x by (x speed)
>   move vertically
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Player** starts moving.
>
> Press the arrow keys to change direction.
>
> Press `space` to jump, then try pressing `space` again before the **Player** lands.
>
> Check that the **Player** only jumps from the ground. If the **Player** moves too quickly or too slowly, change `move speed` in the starter setup script. If the jump feels too high or too low, change `jump strength`.
