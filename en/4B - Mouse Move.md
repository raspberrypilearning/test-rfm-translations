## 4B - Mouse Move

Make the **Player** follow the mouse on the x-axis and click to jump.

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
> The starter project already includes the `Up Down Helper` block, the **Player** setup script, and these **Player** variables:
>
> `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, `on ground`, `vertical steps`

## Step 4

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> Inside a `forever`{:class="block3control"} loop, set `x speed`{:class="block3variables"} to the distance from the **Player** to the mouse pointer, divided by `4`.
>
> ```blocks3
> +when green flag clicked
> +forever
> +  set [x speed v] to (((mouse x) - (x position)) / (4))
> +end
> ```

## Step 5

> [!TASK]
>
> Add an `if`{:class="block3control"} block that sets `x speed`{:class="block3variables"} to `0` when the **Player** is close to the mouse pointer.
>
> This stops the **Player** wobbling when it reaches the mouse pointer.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
> +  if <([abs v] of ((mouse x) - (x position))) < (2)> then
> +    set [x speed v] to (0)
> +  end
> end
> ```

## Step 6

> [!TASK]
>
> Add two `if`{:class="block3control"} blocks so the **Player** points in the direction it is moving.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
>   if <([abs v] of ((mouse x) - (x position))) < (2)> then
>     set [x speed v] to (0)
>   end
>
> +  if <(x speed) > (0)> then
> +    point in direction (90)
> +  end
>
> +  if <(x speed) < (0)> then
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
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
>   if <([abs v] of ((mouse x) - (x position))) < (2)> then
>     set [x speed v] to (0)
>   end
>
>   if <(x speed) > (0)> then
>     point in direction (90)
>   end
>
>   if <(x speed) < (0)> then
>     point in direction (-90)
>   end
>
> +  change x by (x speed)
> end
> ```

## Step 8

> [!TASK]
>
> Above `change x by (x speed)`{:class="block3motion"}, add an `if`{:class="block3control"} block that checks whether the mouse button is pressed.
>
> Inside the `if`{:class="block3control"} block, set `y speed`{:class="block3variables"} to `jump strength`{:class="block3variables"}.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
>   if <([abs v] of ((mouse x) - (x position))) < (2)> then
>     set [x speed v] to (0)
>   end
>
>   if <(x speed) > (0)> then
>     point in direction (90)
>   end
>
>   if <(x speed) < (0)> then
>     point in direction (-90)
>   end
>
> +  if <mouse down?> then
> +    set [y speed v] to (jump strength)
> +  end
>
>   change x by (x speed)
> end
> ```

## Step 9

> [!TASK]
>
> At the bottom of the `forever`{:class="block3control"} loop, add the `Up Down Helper` block from **My Blocks**.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
>   if <([abs v] of ((mouse x) - (x position))) < (2)> then
>     set [x speed v] to (0)
>   end
>
>   if <(x speed) > (0)> then
>     point in direction (90)
>   end
>
>   if <(x speed) < (0)> then
>     point in direction (-90)
>   end
>
>   if <mouse down?> then
>     set [y speed v] to (jump strength)
>   end
>
>   change x by (x speed)
> +  Up Down Helper
> end
> ```

## Step 10

> [!TASK]
>
> Click the green flag and test your controls.
>
> Click the mouse button to jump, then click again while the **Player** is still in the air.
>
> You should see that the **Player** can jump again before landing. This is called a double jump.

## Step 11

> [!TASK]
>
> To stop the double jump, add an `and`{:class="block3operators"} condition to the mouse button `if`{:class="block3control"} block.
>
> The **Player** should only jump if the mouse button is pressed and `on ground`{:class="block3variables"} is `1`.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (((mouse x) - (x position)) / (4))
>
>   if <([abs v] of ((mouse x) - (x position))) < (2)> then
>     set [x speed v] to (0)
>   end
>
>   if <(x speed) > (0)> then
>     point in direction (90)
>   end
>
>   if <(x speed) < (0)> then
>     point in direction (-90)
>   end
>
> -  if <mouse down?> then
> +  if <<mouse down?> and <(on ground) = (1)>> then
>     set [y speed v] to (jump strength)
>   end
>
>   change x by (x speed)
>   Up Down Helper
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> Click to jump, then try clicking again before the **Player** lands.
>
> Check that the **Player** follows the mouse smoothly and only jumps from the ground. If it moves too slowly or too quickly, change the `4` in the division block.
