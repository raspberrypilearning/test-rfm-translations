## 7A - Place Collectables

Place collectables exactly where you want the player to find them.

## Step 1

> [!TASK]
>
> Add or choose a collectable sprite.
>
> You can use a coin, star, gem, crystal, or any other small object.
>
> If your collectable has different looks, add or rename its costumes. The example below uses `Crystal-a` and `Crystal-b`.
>
> ![A coin collectable sprite.](images/coin.png){:width="300px"}
>
> ![A star collectable sprite.](images/star.png){:width="300px"}

## Step 2

> [!TASK]
>
> Select the collectable sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 3

> [!TASK]
>
> Add blocks to move the collectable to its first position, show it, and create a clone.
>
> Change the costume and position to match your own collectable. This example uses crystals.
>
> ```blocks3
> when green flag clicked
> +go to x: (-4) y: (100)
> +show
> +create clone of [myself v]
> ```

## Step 4

> [!TASK]
>
> Add more `go to x: y:`{:class="block3motion"} and `create clone of [myself v]`{:class="block3control"} blocks for each extra collectable.
>
> Put each clone somewhere the **Player** can reach.
>
> ```blocks3
> when green flag clicked
> go to x: (-4) y: (100)
> show
> create clone of [myself v]
> +go to x: (160) y: (100)
> +create clone of [myself v]
> +go to x: (-170) y: (100)
> +create clone of [myself v]
> ```

## Step 5

> [!TASK]
>
> Add `go to [front v] layer`{:class="block3looks"} so they appear in front of any platforms and then add a `hide`{:class="block3looks"} block to the bottom of the green flag script so the original sprite disappears after it has made all the clones.
>
> ```blocks3
> when green flag clicked
> go to x: (-4) y: (100)
> show
> create clone of [myself v]
> go to x: (160) y: (100)
> create clone of [myself v]
> go to x: (-170) y: (100)
> create clone of [myself v]
> +go to [front v] layer
> +hide
> ```

## Step 6

> [!TASK]
>
> Add a second script to the collectable sprite that starts when each clone is created.
>
> ```blocks3
> +when I start as a clone
> ```

## Step 7

> [!TASK]
>
> Add `show`{:class="block3looks"} and `go to [front v] layer`{:class="block3looks"} so each clone appears in front of the level.
>
> ```blocks3
> when I start as a clone
> +show
> +go to [front v] layer
> ```

## Step 8

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop with an `if`{:class="block3control"} block that checks whether the collectable clone is touching the **Player**.
>
> ```blocks3
> when I start as a clone
> show
> go to [front v] layer
> +forever
> +  if <touching [Player v]?> then
> +  end
> +end
> ```

## Step 9

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add `change [Score v] by (1)`{:class="block3variables"} and `hide`{:class="block3looks"}.
>
> ```blocks3
> when I start as a clone
> show
> go to [front v] layer
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
> Click the green flag and check that each collectable appears where you placed it.
>
> Touch each collectable and check that it disappears and adds `1` to `Score`.
