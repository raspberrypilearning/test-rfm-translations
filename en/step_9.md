## 4A - Keys

Add keyboard controls so the **Player** can run and jump.

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
> Add this keyboard movement script.
>
> ```blocks3
> when green flag clicked
> forever
>   set [x speed v] to (0)
>
>   if <<key [d v] pressed?> or <key [right arrow v] pressed?>> then
>     set [x speed v] to (move speed)
>     point in direction (90)
>   end
>
>   if <<key [a v] pressed?> or <key [left arrow v] pressed?>> then
>     set [x speed v] to ((0) - (move speed))
>     point in direction (-90)
>   end
>
>   change x by (x speed)
> end
> ```

## Step 5

> [!TASK]
>
> Add this jump and fall script.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Platform v]?> then
>     change x by ((0) - (x speed))
>   end
>
>   if <<key [space v] pressed?> and <(on ground) = (1)>> then
>     set [y speed v] to (jump strength)
>   end
>
>   move vertically
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and use `A` and `D`, or the arrow keys, to move.
>
> Press `space` to jump. If the **Player** moves too quickly or too slowly, change `move speed` in the starter setup script. If the jump feels too high or too low, change `jump strength`.
