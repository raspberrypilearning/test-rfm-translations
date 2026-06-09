## 7C - Take Key to Exit

Make the player win only after collecting a key and reaching the **Exit**.

## Step 1

> [!TASK]
>
> Make sure you have a variable called `has key`.
>
> Set it up for all sprites so the Stage, **Key**, and **Exit** sprites can all use it.

## Step 2

> [!TASK]
>
> Place the key somewhere interesting and put the exit where the player can reach it after collecting the key.
>
> ![A key sprite.](images/key.png){:width="300px"}
>
> ![An exit door sprite.](images/exit-door.png){:width="300px"}

## Step 3

> [!TASK]
>
> Select the **Stage** and add a script that starts when the green flag is clicked.
>
> ```blocks3
> when green flag clicked
> set [has key v] to [0]
> ```

## Step 4

> [!TASK]
>
> Select the **Key** sprite and add this script.
>
> ```blocks3
> when green flag clicked
> show
> forever
>   if <touching [Player v]?> then
>     set [has key v] to [1]
>     hide
>   end
> end
> ```

## Step 5

> [!TASK]
>
> Select the **Exit** sprite and add a script that checks when the player touches it.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
>   end
> end
> ```

## Step 6

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add another `if`{:class="block3control"} block to check whether `has key` is `1`.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
> +    if <(has key) = [1]> then
> +    else
> +    end
>   end
> end
> ```

## Step 7

> [!TASK]
>
> In the `has key = 1` part, add `broadcast [win v]`{:class="block3events"}, `say [Unlocked!] for (2) seconds`{:class="block3looks"}, and `stop [this script v]`{:class="block3control"}.
>
> In the `else` part, add a `say [] for (2) seconds`{:class="block3looks"} block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
>     if <(has key) = [1]> then
> +      broadcast [win v]
> +      say [Unlocked!] for (2) seconds
> +      stop [this script v]
>     else
> +      say [] for (2) seconds
>     end
>   end
> end
> ```

## Test

> [!TASK]
>
> Touch the exit before and after collecting the key to check that only the keyed route wins.
