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
> Inside the `if`{:class="block3control"} block, add `broadcast win`{:class="block3events"}.
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
> Add a new script that starts when it receives the `win`{:class="block3events"} message.
>
> Add `say 'You win!' for 2 seconds`{:class="block3looks"} and `stop all`{:class="block3control"}.
>
> ```blocks3
> +when I receive [win v]
> +say [You win!] for (2) seconds
> +stop [all v]
> ```

## Step 7

> [!TASK]
>
> Choose what should happen before `stop all`{:class="block3control"}.
>
> You can use the `when I receive win`{:class="block3events"} script to show a message, play a sound, change backdrop, switch costume, or trigger another sprite before the game stops.
>
> Put any extra win blocks above `stop all`{:class="block3control"}.

## Test

> [!TASK]
>
> Move the **Player** to the **Exit** and check that the win message appears and the game stops.
