## 8B - Target Score

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
> Set it up for **all sprites** so the Stage and collectable sprite can both use it.

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
> Add a `forever`{:class="block3control"} loop below the variable setup block.
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
> Inside the `forever`{:class="block3control"} loop, add an `if`{:class="block3control"} block that checks whether `Score` is equal to your target value.
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
> Inside the `if`{:class="block3control"} block, add `broadcast win`{:class="block3events"}.
>
> ```blocks3
> when green flag clicked
> set [Score v] to [0]
> forever
>   if <(Score) = ()> then
> +    broadcast [win v]
>   end
> end
> ```

## Step 8

> [!TASK]
>
> Add a new script that starts when it receives the `win`{:class="block3events"} message.
>
> Add `say 'You win!' for 2 seconds`{:class="block3looks"} and `stop all`{:class="block3control"}.
>
> If you already added this win script in another route, just check this step off.
>
> ```blocks3
> +when I receive [win v]
> +say [You win!] for (2) seconds
> +stop [all v]
> ```

## Step 9

> [!TASK]
>
> Choose what should happen before `stop all`{:class="block3control"}.
>
> You can use the `when I receive win`{:class="block3events"} script to show a message, play a sound, change backdrop, switch costume, or trigger another sprite before the game stops.
>
> Put any extra win blocks above `stop all`{:class="block3control"}.

## Step 10

> [!TASK]
>
> **Select the collectable sprite** and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 11

> [!TASK]
>
> Add a `show`{:class="block3looks"} block and a `forever`{:class="block3control"} loop.
>
> ```blocks3
> when green flag clicked
> +show
> +forever
> +end
> ```

## Step 12

> [!TASK]
>
> Inside the `forever`{:class="block3control"} loop, add an `if`{:class="block3control"} block that checks whether the collectable is touching the **Player**.
>
> ```blocks3
> when green flag clicked
> show
> forever
> +  if <touching [Player v]?> then
> +  end
> end
> ```

## Step 13

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add `change Score by 1`{:class="block3variables"} and `hide`{:class="block3looks"}.
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
> Collect enough items and check that the `win`{:class="block3events"} message broadcasts, the win message appears, and the game stops.
