## 8C - Take Key to Exit

Make the player win only after collecting a key and reaching the **Exit**.

## Step 1

> [!TASK]
>
> Make sure you have a variable called `has key`.
>
> Set it up for all sprites so the Stage, **Key**, and **Exit** sprites can all use it.

## Step 2

> [!TASK]
>
> Place the key somewhere interesting and put the exit where the player can reach it after collecting the key.
>
> ![A key sprite.](images/key.png){:width="300px"}
>
> ![An exit door sprite.](images/exit-door.png){:width="300px"}

## Step 3

> [!TASK]
>
> Select the **Stage** and add a script that starts when the green flag is clicked.
>
> ```blocks3
> when green flag clicked
> set [has key v] to [0]
> ```

## Step 4

> [!TASK]
>
> Select the **Key** sprite and add this script.
>
> ```blocks3
> when green flag clicked
> show
> forever
>   if <touching [Player v]?> then
>     set [has key v] to [1]
>     hide
>   end
> end
> ```

## Step 5

> [!TASK]
>
> Select the **Exit** sprite and add a script that checks when the player touches it.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
>   end
> end
> ```

## Step 6

> [!TASK]
>
> Inside the `if`{:class="block3control"} block, add another `if`{:class="block3control"} block to check whether `has key` is `1`.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
> +    if <(has key) = [1]> then
> +    else
> +    end
>   end
> end
> ```

## Step 7

> [!TASK]
>
> In the `has key = 1` part, add `broadcast win`{:class="block3events"}.
>
> In the `else` part, add a `say 'Find the key!' for 2 seconds`{:class="block3looks"} block.
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Player v]?> then
>     if <(has key) = [1]> then
> +      broadcast [win v]
>     else
> +      say [Find the key!] for (2) seconds
>     end
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

## Test

> [!TASK]
>
> Touch the exit before and after collecting the key.
>
> Check that the keyed route broadcasts `win`{:class="block3events"}, shows the win message, and stops the game only after the key has been collected.
