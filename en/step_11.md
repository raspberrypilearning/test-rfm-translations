## 4B - Mouse Move

Make the **Player** follow the mouse on the x-axis.

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
> The starter project already includes the **Player** setup script and the `x speed`{:class="block3variables"} variable.
>
> If you can already see it in your starter project, just check this step off.

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

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> Check that the **Player** follows the mouse smoothly on the x-axis. If it moves too slowly or too quickly, change the `4` in the division block.
