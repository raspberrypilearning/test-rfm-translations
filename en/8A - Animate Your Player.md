## 8A - Animate Your Player

Switch costumes while the **Player** moves so the character feels more alive.

## Step 1

> [!TASK]
>
> Select the **Player** sprite and open the **Costumes** tab.
>
> Check that the sprite has more than one costume.
>
> ![The Costumes tab in Scratch.](images/costume_tab.png)

## Step 2

> [!TASK]
>
> Open the **Code** tab and add this animation script.
>
> ```blocks3
> when green flag clicked
> forever
>   if <<not <(x speed) = (0)>> and <(on ground) = (1)>> then
>     next costume
>     wait () seconds
>   end
> end
> ```
>
> Type your own delay into the `wait`{:class="block3control"} block.

## Test

> [!TASK]
>
> Move the **Player** and check that the costume changes while it travels.
