## 8A - Get to Exit Sprite (Default)

Make the player win when they touch the **Exit** sprite.

## Step 1

> [!TASK]
>
> Select the **Player** sprite in the sprite pane.

## Step 2

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 3

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop below the green flag block.
>
> ```blocks3
> when green flag clicked
> +forever
> +end
> ```

## Step 4

> [!TASK]
>
> Inside the `forever`{:class="block3control"} loop, add an `if`{:class="block3control"} block that checks whether the **Player** is touching the **Exit** sprite.
>
> ```blocks3
> when green flag clicked
> forever
> +  if <touching [Exit v]?> then
> +  end
> end
> ```

## Step 5

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add `broadcast [win v]`{:class="block3events"}.
>
> This lets other routes react to the win later.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Exit v]?> then
> +    broadcast [win v]
>   end
> end
> ```

## Step 6

> [!TASK]
>
> Add `stop [this script v]`{:class="block3control"} below the broadcast block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Exit v]?> then
>     broadcast [win v]
> +    stop [this script v]
>   end
> end
> ```

## Test

> [!TASK]
>
> Move the **Player** to the **Exit** and check that the win message appears.
