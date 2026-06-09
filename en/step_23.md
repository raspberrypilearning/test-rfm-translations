## 9B - Make Your Player Sprint

Add a sprint key to the keyboard controls from `4A - Keys`.

## Step 1

> [!TASK]
>
> This extra works with `4A - Keys`.
>
> If you chose `4B - Mouse Move` or `4C - Always Moving`, skip this extra and choose a different one.

## Step 2

> [!TASK]
>
> Make a variable called `sprint speed` for the **Player** sprite.

## Step 3

> [!TASK]
>
> Replace the movement script from `4A - Keys` with this version.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to (5)
> set [sprint speed v] to (8)
> forever
>   set [x speed v] to (0)
>
>   if <key [shift v] pressed?> then
>     if <<key [d v] pressed?> or <key [right arrow v] pressed?>> then
>       set [x speed v] to (sprint speed)
>       point in direction (90)
>     end
>     if <<key [a v] pressed?> or <key [left arrow v] pressed?>> then
>       set [x speed v] to ((0) - (sprint speed))
>       point in direction (-90)
>     end
>   else
>     if <<key [d v] pressed?> or <key [right arrow v] pressed?>> then
>       set [x speed v] to (move speed)
>       point in direction (90)
>     end
>     if <<key [a v] pressed?> or <key [left arrow v] pressed?>> then
>       set [x speed v] to ((0) - (move speed))
>       point in direction (-90)
>     end
>   end
>
>   change x by (x speed)
> end
> ```

## Test

> [!TASK]
>
> Hold `shift` while moving and check that the **Player** travels faster.
