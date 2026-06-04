## 7A - Get to Exit Sprite (Default)

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
> Add a `forever` loop below the green flag block.
>
> ```blocks3
> when green flag clicked
> +forever
> +end
> ```

## Step 4

> [!TASK]
>
> Inside the `forever` loop, add an `if` block that checks whether the **Player** is touching the **Exit** sprite.
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
> Inside the `if` block, add `broadcast [win v]`.
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
> Add `stop [this script v]` below the broadcast block.
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
