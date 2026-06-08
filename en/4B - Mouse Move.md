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
> The starter project already includes the `move vertically` block, the **Player** setup script, and these **Player** variables:
>
> `x speed`, `y speed`, `gravity`, `jump strength`, `move speed`, `on ground`, `vertical steps`
>
> If you can already see them in your starter project, just check this step off.

## Step 4

> [!TASK]
>
> Add this mouse movement script.
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
>   if <(x speed) < (0)> then
>     point in direction (-90)
>   end
>
>   change x by (x speed)
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> Check that the **Player** follows the mouse smoothly. If it moves too slowly or too quickly, change the `4` in the division block.
