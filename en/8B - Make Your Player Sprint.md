## 8B - Make Your Player Sprint

Add a sprint control so the **Player** can move faster when a key is pressed.

## Step 1

> [!TASK]
>
> Make variables called `move speed` and `sprint speed` for the **Player** sprite.

## Step 2

> [!TASK]
>
> Select the **Player** sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 3

> [!TASK]
>
> Add blocks to set `move speed` and `sprint speed` to your own values.
>
> ```blocks3
> when green flag clicked
> +set [move speed v] to ()
> +set [sprint speed v] to ()
> ```

## Step 4

> [!TASK]
>
> Add a `forever` loop below the variable setup blocks.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> set [sprint speed v] to ()
> +forever
> +end
> ```

## Step 5

> [!TASK]
>
> Inside the `forever` loop, add an `if else` block that checks whether the `shift` key is pressed.
>
> This lets `shift` act as the sprint key.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> set [sprint speed v] to ()
> forever
> +  if <key [shift v] pressed?> then
> +  else
> +  end
> end
> ```

## Step 6

> [!TASK]
>
> In the `shift pressed` part, add movement code that uses `sprint speed`.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> set [sprint speed v] to ()
> forever
>   if <key [shift v] pressed?> then
> +    if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
> +      change x by (sprint speed)
> +    end
> +    if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +      change x by ((0) - (sprint speed))
> +    end
>   else
>   end
> end
> ```

## Step 7

> [!TASK]
>
> In the `else` part, add movement code that uses `move speed`.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> set [sprint speed v] to ()
> forever
>   if <key [shift v] pressed?> then
>     if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>       change x by (sprint speed)
>     end
>     if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
>       change x by ((0) - (sprint speed))
>     end
>   else
> +    if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
> +      change x by (move speed)
> +    end
> +    if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +      change x by ((0) - (move speed))
> +    end
>   end
> end
> ```

## Test

> [!TASK]
>
> Hold `shift` while moving and check that the **Player** travels faster.
