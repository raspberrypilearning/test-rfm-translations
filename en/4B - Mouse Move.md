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

The starter project already includes an `Up Down Helper` block, and the **Player** setup script with these **player** variables:

`x speed`{:class="block3variables"}, `y speed`{:class="block3variables"}, `gravity`{:class="block3variables"}, `jump strength`{:class="block3variables"}, `move speed`{:class="block3variables"}, `on ground`, `vertical steps`{:class="block3variables"}

## Step 3

> [!TASK]
>
> Inside a `forever`{:class="block3control"} loop, point the **player** at the mouse-pointer.
>
> ```blocks3
> when green flag clicked
> go to x: (100) y: (100)
> +forever
> +point towards (mouse-pointer v)
> +end
> ```

## Step 4

> [!TASK]
>
> The **player** sprite is going to move towards the mouse-pointer, but only letf and right.
>
> ```blocks3
> when green flag clicked
> go to x: (100) y: (100)
> forever
> point towards (mouse-pointer v)
> set [x speed v] to ((mouse x) - (x position))
> +end
> ```

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> The sprite should always be at about the same x position as the mouse-pointer.
>
> 

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
