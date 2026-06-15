## 5B - Player Jump-Fall (Mouse)

Add click-to-jump and falling to the mouse controls from `4B - Mouse Move`.

## Step 1

> [!TASK]
>
> This step works with `4B - Mouse Move`.
>
> If you chose `4A - Keys` or `4C - Always Moving`, use `5A - Player Jump-Fall (Keys)` instead.

## Step 2

> [!TASK]
>
> The starter project already includes the `Up Down Helper` block and these **Player** variables:
>
> `y speed`, `gravity`, `jump strength`, `on ground`, `vertical steps`
>
> If you can already see them in your starter project, just check this step off.

## Step 3

> [!TASK]
>
> Find the mouse movement script from `4B - Mouse Move`.
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

## Step 4

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

## Step 5

> [!TASK]
>
> Click the green flag and test your controls.
>
> Click the mouse button to jump, then click again while the **Player** is still in the air.
>
> You should see that the **Player** can jump again before landing. This is called a double jump.

## Step 6

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

## Step 7

> [!TASK]
>
> Find the starter setup script for the **Player**.
>
> Look for this block.
>
> ```blocks3
> set [jump strength v] to (14)
> ```
>
> Change `14` if you want a higher or lower jump.

## Step 8

> [!TASK]
>
> Look for this block in the same setup script.
>
> ```blocks3
> set [gravity v] to (-1)
> ```
>
> Change `-1` if you want a faster or slower fall. A more negative number makes stronger gravity.

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> Click to jump, then try clicking again before the **Player** lands.
>
> Check that the **Player** follows the mouse smoothly and only jumps from the ground.
>
> Keep adjusting `jump strength` and `gravity` until the **Player** feels right for your level.
