## 7B - Target Score

Make the player win after their **Score** reaches a target value.

## Step 1

> [!TASK]
>
> Add or choose a collectable sprite.
>
> You can use a coin, star, gem, or any other small object.
>
> ![A coin collectable sprite.](images/coin.png){:width="300px"}
>
> ![A star collectable sprite.](images/star.png){:width="300px"}

## Step 2

> [!TASK]
>
> Make sure you have a variable called `Score`.
>
> Set it up for all sprites so the Stage and collectable sprite can both use it.

## Step 3

> [!TASK]
>
> Select the **Stage** and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 4

> [!TASK]
>
> Add a block to set `Score` to `0`.
>
> ```blocks3
> when green flag clicked
> +set [Score v] to [0]
> ```

## Step 5

> [!TASK]
>
> Add a `forever` loop below the variable setup block.
>
> ```blocks3
> when green flag clicked
> set [Score v] to [0]
> +forever
> +end
> ```

## Step 6

> [!TASK]
>
> Inside the `forever` loop, add an `if` block that checks whether `Score` is equal to your target value.
>
> Type your target score into the white input.
>
> ```blocks3
> when green flag clicked
> set [Score v] to [0]
> forever
> +  if <(Score) = ()> then
> +  end
> end
> ```

## Step 7

> [!TASK]
>
> Inside the `if` block, add `broadcast [win v]` and `stop [this script v]`.
>
> ```blocks3
> when green flag clicked
> set [Score v] to [0]
> forever
>   if <(Score) = ()> then
> +    broadcast [win v]
> +    stop [this script v]
>   end
> end
> ```

## Step 8

> [!TASK]
>
> Select the collectable sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 9

> [!TASK]
>
> Add a `show` block and a `forever` loop.
>
> ```blocks3
> when green flag clicked
> +show
> +forever
> +end
> ```

## Step 10

> [!TASK]
>
> Inside the `forever` loop, add an `if` block that checks whether the collectable is touching the **Player**.
>
> ```blocks3
> when green flag clicked
> show
> forever
> +  if <touching [Player v]?> then
> +  end
> end
> ```

## Step 11

> [!TASK]
>
> Inside the `if` block, add `change [Score v] by (1)` and `hide`.
>
> ```blocks3
> when green flag clicked
> show
> forever
>   if <touching [Player v]?> then
> +    change [Score v] by (1)
> +    hide
>   end
> end
> ```

## Test

> [!TASK]
>
> Collect enough items and check that `win` broadcasts when the value of `Score` matches your target value.
