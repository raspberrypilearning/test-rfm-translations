## 4A - Keys

Add keyboard controls so the **Player** can move left and right.

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
> Make a variable called `move speed` for the **Player** sprite.
>
> This variable controls how far the **Player** moves each time the loop runs. You will choose your own speed in the white input.

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
> Add a block to set the `move speed`.
>
> ```blocks3
> when green flag clicked
> +set [move speed v] to ()
> ```

## Step 6

> [!TASK]
>
> Add a `forever` loop below the `set [move speed v] to ()` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> +forever
> +end
> ```

## Step 7

> [!TASK]
>
> Inside the `forever` loop, add an empty `if` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
> +  if <> then
> +  end
> end
> ```

## Step 8

> [!TASK]
>
> Add an `or` operator block to the `if` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
> +  if <<> or <>> then
>   end
> end
> ```

## Step 9

> [!TASK]
>
> Add a `key [right arrow v] pressed?` sensing block to the first side of the `or` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
> +  if <<key [right arrow v] pressed?> or <>> then
>   end
> end
> ```

## Step 10

> [!TASK]
>
> Add a `key [d v] pressed?` sensing block to the second side of the `or` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
> +  if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>   end
> end
> ```

## Step 11

> [!TASK]
>
> Inside the right movement `if` block, add a `change x by` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
> +    change x by ()
>   end
> end
> ```

## Step 12

> [!TASK]
>
> Add the `move speed` variable block to the `change x by` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
> +    change x by (move speed)
>   end
> end
> ```

## Step 13

> [!TASK]
>
> Below the right movement `if` block, add another empty `if` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
> +  if <> then
> +  end
> end
> ```

## Step 14

> [!TASK]
>
> Add an `or` operator block to the new `if` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
> +  if <<> or <>> then
>   end
> end
> ```

## Step 15

> [!TASK]
>
> Add a `key [left arrow v] pressed?` sensing block to the first side of the `or` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
> +  if <<key [left arrow v] pressed?> or <>> then
>   end
> end
> ```

## Step 16

> [!TASK]
>
> Add a `key [a v] pressed?` sensing block to the second side of the `or` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
> +  if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
>   end
> end
> ```

## Step 17

> [!TASK]
>
> Inside the left movement `if` block, add a `change x by` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
>   if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +    change x by ()
>   end
> end
> ```

## Step 18

> [!TASK]
>
> Add a subtract operator block to the `change x by` block.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
>   if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +    change x by ((0) - ())
>   end
> end
> ```

## Step 19

> [!TASK]
>
> Add the `move speed` variable block to the second side of the subtract operator.
>
> ```blocks3
> when green flag clicked
> set [move speed v] to ()
> forever
>   if <<key [right arrow v] pressed?> or <key [d v] pressed?>> then
>     change x by (move speed)
>   end
>   if <<key [left arrow v] pressed?> or <key [a v] pressed?>> then
> +    change x by ((0) - (move speed))
>   end
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and try the left and right controls.
>
> If the **Player** moves too slowly or too quickly, change the number in the `set [move speed v] to ()` block.

