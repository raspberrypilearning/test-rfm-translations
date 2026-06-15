## 7B - Random Collectables

Make collectables drop from random positions and land on the **Platform** sprite.

## Step 1

> [!TASK]
>
> Add or choose a collectable sprite.
>
> You can use a coin, star, gem, crystal, or any other small object.
>
> ![A coin collectable sprite.](images/coin.png){:width="300px"}
>
> ![A star collectable sprite.](images/star.png){:width="300px"}

## Step 2

> [!TASK]
>
> Make sure you have these variables:
>
> `Score`, `last_x`, `min_distance`, and `position_ok`
>
> Make `Score` for all sprites. The other variables are used by the collectable sprite to choose and space out the clones.
>
> Use these exact names so the blocks below match.

## Step 3

> [!TASK]
>
> Select the collectable sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 4

> [!TASK]
>
> Hide the original collectable sprite, reset `Score`, and set up the variables that space out the collectables.
>
> The hidden original sprite will move to random x and y positions and create visible clones.
>
> ```blocks3
> when green flag clicked
> +hide
> +set [Score v] to (0)
> +set [last_x v] to (999)
> +set [min_distance v] to (70)
> +set [position_ok v] to (0)
> ```

## Step 5

> [!TASK]
>
> Add a `repeat`{:class="block3control"} loop for the number of collectables you want to create at the start.
>
> This example creates `5` collectables.
>
> ```blocks3
> when green flag clicked
> hide
> set [Score v] to (0)
> set [last_x v] to (999)
> set [min_distance v] to (70)
> set [position_ok v] to (0)
> +repeat (5)
> +end
> ```

## Step 6

> [!TASK]
>
> Inside the `repeat`{:class="block3control"} loop, set `position_ok`{:class="block3variables"} to `0`{:class="block3variables"} and add a `repeat until`{:class="block3control"} loop that chooses a random start position.
>
> The hidden original keeps choosing until it is at least `min_distance` away from the previous collectable.
>
> Use random y positions so collectables can start below higher platforms and land on lower ones.
>
> The hidden original briefly shows itself to test whether it is touching the **Platform**, then hides again before it creates the clone. If the random start position is already touching the **Platform**, the loop chooses another position.
>
> ```blocks3
> when green flag clicked
> hide
> set [Score v] to (0)
> set [last_x v] to (999)
> set [min_distance v] to (70)
> set [position_ok v] to (0)
> repeat (5)
> +  set [position_ok v] to (0)
> +  repeat until <(position_ok) = (1)>
> +    go to x: (pick random (-200) to (200)) y: (pick random (-120) to (160))
> +    show
> +    if <<<not <touching [Platform v]?>> and <<(x position) > ((last_x) + (min_distance))> or <(x position) < ((last_x) - (min_distance))>>> then
> +      set [position_ok v] to (1)
> +    end
> +    hide
> +  end
> end
> ```

## Step 7

> [!TASK]
>
> After the `repeat until`{:class="block3control"} loop, store the chosen x position as `last_x` and create a clone there.
>
> ```blocks3
> when green flag clicked
> hide
> set [Score v] to (0)
> set [last_x v] to (999)
> set [min_distance v] to (70)
> set [position_ok v] to (0)
> repeat (5)
>   set [position_ok v] to (0)
>   repeat until <(position_ok) = (1)>
>     go to x: (pick random (-200) to (200)) y: (pick random (-120) to (160))
>     show
>     if <<<not <touching [Platform v]?>> and <<(x position) > ((last_x) + (min_distance))> or <(x position) < ((last_x) - (min_distance))>>> then
>       set [position_ok v] to (1)
>     end
>     hide
>   end
> +  set [last_x v] to (x position)
> +  create clone of [myself v]
> end
> ```

## Step 8

> [!TASK]
>
> Add a second script to the collectable sprite that starts when each clone is created.
>
> ```blocks3
> +when I start as a clone
> ```

## Step 9

> [!TASK]
>
> Add `show`{:class="block3looks"} and a `repeat until`{:class="block3control"} loop that makes the clone fall straight down until it touches the **Platform** sprite.
>
>
> ```blocks3
> when I start as a clone
> +show
> +repeat until <touching [Platform v]?>
> +  change y by (-10)
> +end
> ```

## Step 10

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop with an `if`{:class="block3control"} block that checks whether the collectable clone is touching the **Player**.
>
> The screenshot shows the random drop setup. Add this part so each clone can be collected.
>
> ```blocks3
> when I start as a clone
> show
> repeat until <touching [Platform v]?>
>   change y by (-10)
> end
> +forever
> +  if <touching [Player v]?> then
> +  end
> +end
> ```

## Step 11

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add `change [Score v] by (1)`{:class="block3variables"} and `hide`{:class="block3looks"}.
>
> ```blocks3
> when I start as a clone
> show
> repeat until <touching [Platform v]?>
>   change y by (-10)
> end
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
> Click the green flag and check that collectables drop from random positions, spaced apart from each other.
>
> Check that each collectable starts in the air, drops, and stops when it touches the **Platform** sprite.
>
> Touch a collectable and check that it disappears and adds `1` to `Score`.
