## 5A - Player Jump/Fall (Simple)

Add a quick jump and fall motion without building a full gravity system.

## Step 1

> [!TASK]
>
> Select the **Player** sprite in the sprite pane.

## Step 2

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

## Step 3

> [!TASK]
>
> Decide how high and how fast the **Player** should jump.
>
> You will type your own repeat counts and movement amounts into the white inputs. Larger numbers make a higher or faster jump.

## Step 4

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 5

> [!TASK]
>
> Add a `forever` loop below the green flag block.
>
> ```blocks3
> when green flag clicked
> +forever
> +end
> ```

## Step 6

> [!TASK]
>
> Inside the `forever` loop, add an empty `if` block.
>
> ```blocks3
> when green flag clicked
> forever
> +  if <> then
> +  end
> end
> ```

## Step 7

> [!TASK]
>
> Add a `key [space v] pressed?` sensing block to the `if` block.
>
> ```blocks3
> when green flag clicked
> forever
> +  if <key [space v] pressed?> then
>   end
> end
> ```

## Step 8

> [!TASK]
>
> Inside the space key `if` block, add a repeat loop for moving up.
>
> ```blocks3
> when green flag clicked
> forever
>   if <key [space v] pressed?> then
> +    repeat ()
> +    end
>   end
> end
> ```

## Step 9

> [!TASK]
>
> Inside the repeat loop, add a `change y by` block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <key [space v] pressed?> then
>     repeat ()
> +      change y by ()
>     end
>   end
> end
> ```

## Step 10

> [!TASK]
>
> Below the first repeat loop, add a second repeat loop for moving back down.
>
> ```blocks3
> when green flag clicked
> forever
>   if <key [space v] pressed?> then
>     repeat ()
>       change y by ()
>     end
> +    repeat ()
> +    end
>   end
> end
> ```

## Step 11

> [!TASK]
>
> Inside the second repeat loop, add a `change y by` block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <key [space v] pressed?> then
>     repeat ()
>       change y by ()
>     end
>     repeat ()
> +      change y by ()
>     end
>   end
> end
> ```

## Step 12

> [!TASK]
>
> Add a subtract operator block to the second `change y by` block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <key [space v] pressed?> then
>     repeat ()
>       change y by ()
>     end
>     repeat ()
> +      change y by ((0) - ())
>     end
>   end
> end
> ```


## Test

> [!TASK]
>
> Click the green flag and press space.
>
> If the **Player** jumps too high, too low, too quickly, or too slowly, change the numbers in the repeat loops and `change y by` blocks.

