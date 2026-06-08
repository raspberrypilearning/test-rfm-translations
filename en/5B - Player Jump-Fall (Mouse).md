## 5B - Player Jump/Fall (Mouse)

Add jumping and falling to the mouse movement from `4B - Mouse Move`.

## Step 1

> [!TASK]
>
> This step works with `4B - Mouse Move`.
>
> If you chose `4A - Keys` or `4C - Always Moving`, skip this option and choose a different jump/fall step.

## Step 2

> [!TASK]
>
> Select the **Player** sprite in the sprite pane.

## Step 3

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

## Step 4

> [!TASK]
>
> Add this mouse jump and fall script.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Platform v]?> then
>     change x by ((0) - (x speed))
>   end
>
>   if <<mouse down?> and <(on ground) = (1)>> then
>     set [y speed v] to (jump strength)
>   end
>
>   move vertically
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and move the mouse left and right.
>
> Click or hold the mouse button to jump. Check that the **Player** lands properly on the **Platform** sprite. If the jump feels too high or too low, change `jump strength` in the setup script.
