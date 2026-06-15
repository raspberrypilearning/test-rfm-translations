## 10E - Make Your Player Sprint

Add a sprint key so the **Player** moves faster while `shift` is held.

## Step 1

> [!TASK]
>
> Find the `forever`{:class="block3control"} loop in your **Player** movement script.
>
> If your movement uses `move speed`{:class="block3variables"}, make a new variable called `sprint speed` for the **Player** sprite.
>
> Set `sprint speed`{:class="block3variables"} to a number bigger than `move speed`{:class="block3variables"} in your starting script.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to (5)
> +set [sprint speed v] to (8)
> ```

## Step 2

> [!TASK]
>
> If you used keyboard controls or always-moving controls, add this sprint check just above `change x by (x speed)`{:class="block3motion"}.
>
> ```blocks3
> forever
>   ...
> + if <key [shift v] pressed?> then
> +   if <(x speed) > (0)> then
> +     set [x speed v] to (sprint speed)
> +   end
> +   if <(x speed) < (0)> then
> +     set [x speed v] to ((0) - (sprint speed))
> +   end
> + else
> +   if <(x speed) > (0)> then
> +     set [x speed v] to (move speed)
> +   end
> +   if <(x speed) < (0)> then
> +     set [x speed v] to ((0) - (move speed))
> +   end
> + end
>   change x by (x speed)
> end
> ```
>
> This makes the **Player** speed up while `shift` is held and slow back down when you release it.

## Step 3

> [!TASK]
>
> If you used mouse movement, use this version instead.
>
> Change the block that sets `x speed`{:class="block3variables"} so it uses a smaller divisor while `shift` is pressed.
>
> ```blocks3
> forever
>   point towards (mouse-pointer v)
> + if <key [shift v] pressed?> then
> +   set [x speed v] to (((mouse x) - (x position)) / (5))
> + else
> +   set [x speed v] to (((mouse x) - (x position)) / (10))
> + end
>   change x by (x speed)
> end
> ```
>
> A smaller divisor makes the **Player** follow the mouse more quickly.

## Test

> [!TASK]
>
> Hold `shift` while moving and check that the **Player** travels faster.
