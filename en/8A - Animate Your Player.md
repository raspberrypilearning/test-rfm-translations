## 8A - Animate Your Player

Switch costumes while the **Player** moves so the character feels more alive.

## Step 1

> [!TASK]
>
> Select the **Player** sprite and open the **Costumes** tab.
>
> Check that the sprite has more than one costume.
>
> ![The Costumes tab in Scratch.](images/costume_tab.png)

## Step 2

> [!TASK]
>
> In the movement script, find the `if` block that checks for right movement.
>
> Add a `next costume` block inside it.
>
> ```blocks3
> when green flag clicked
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
> +    next costume
>   end
> end
> ```

## Step 3

> [!TASK]
>
> Add a `wait () seconds` block below `next costume`.
>
> Type your own animation delay into the white input.
>
> ```blocks3
> when green flag clicked
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     next costume
> +    wait () seconds
>   end
> end
> ```

## Step 4

> [!TASK]
>
> Add the same two blocks to the `if` block that checks for left movement.
>
> ```blocks3
> when green flag clicked
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     next costume
>     wait () seconds
>   end
>   if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +    next costume
> +    wait () seconds
>   end
> end
> ```

## Test

> [!TASK]
>
> Move the **Player** and check that the costume changes while it travels.
