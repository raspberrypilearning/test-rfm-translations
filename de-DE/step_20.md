## 7C - Add a Power Up

Add a new sprite that gives the **Player** extra speed or a higher jump when they touch it.

## Step 1

> [!TASK]
>
> Add or choose a new sprite for your power-up.
>
> You could use a lightning bolt, star, potion, or any other sprite that looks special.

## Step 2

> [!TASK]
>
> Name the sprite `Power Up`.

## Step 3

> [!TASK]
>
> Select the **Power Up** sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 4

> [!TASK]
>
> Add blocks to put the **Power Up** where you want it, show it, and move it in front of the level.
>
> Change the `x` and `y` values to place the power-up in your own level.
>
> ```blocks3
> when green flag clicked
> +go to x: (120) y: (-40)
> +show
> +go to [front v] layer
> ```

## Step 5

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop with an `if`{:class="block3control"} block that checks whether the **Power Up** is touching the **Player**.
>
> ```blocks3
> when green flag clicked
> go to x: (120) y: (-40)
> show
> go to [front v] layer
> +forever
> +  if <touching [Player v]?> then
> +  end
> +end
> ```

## Step 6

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, broadcast `power up`{:class="block3events"}, hide the sprite, and stop this script.
>
> ```blocks3
> when green flag clicked
> go to x: (120) y: (-40)
> show
> go to [front v] layer
> forever
>   if <touching [Player v]?> then
> +    broadcast [power up v]
> +    hide
> +    stop [this script v]
>   end
> end
> ```

## Step 7

> [!TASK]
>
> Select the **Player** sprite and add a new script that starts when it receives the `power up`{:class="block3events"} message.
>
> The movement uses `move speed`{:class="block3variables"} to control how fast the **Player** moves and `jump strength`{:class="block3variables"} to control jump height.
>
> Choose one effect for your power-up. The effect will last for `5` seconds.
>
> To make the **Player** move faster, increase `move speed`{:class="block3variables"}:
>
> ```blocks3
> +when I receive [power up v]
> +change [move speed v] by (2)
> +wait (5) seconds
> +change [move speed v] by (-2)
> ```
>
> To make the **Player** jump higher, increase `jump strength`{:class="block3variables"}:
>
> ```blocks3
> +when I receive [power up v]
> +change [jump strength v] by (4)
> +wait (5) seconds
> +change [jump strength v] by (-4)
> ```
>
> You could also do both! Put both `change`{:class="block3variables"} blocks before the `wait`{:class="block3control"} block, then change both variables back after the wait.

## Test

> [!TASK]
>
> Click the green flag and touch the **Power Up** with your **Player**.
>
> Check that the power-up disappears and the **Player** moves faster or jumps higher for `5` seconds, then goes back to normal.
