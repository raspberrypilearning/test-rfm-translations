<h2 class="c-project-heading--task">9D - Add Hazards</h2>

Add a moving hazard that creates a danger.

## Step 1

> [!TASK]
>
> Create a new sprite and give it a name.

## Step 2

> [!TASK]
>
> In the **paint window**, resize and place the **hazard** sprite above or beside a risky part of the level.

## Step 3

> [!TASK]
>
> Add the blocks below to the **Hazard** sprite.
>
> You can type your own `glide`{:class="block3motion"} time, and `x`{:class="block3motion"} and `y`{:class="block3motion"} positions. Also, add a `wait`{:class="block3control"} time.
>
> ```blocks3
> when green flag clicked
> go to x: () y: ()
> forever
>   glide () secs to x: () y: ()
>   go to x: () y: ()
>   wait () seconds
> end
> ```

## Step 4

> [!TASK]
>
> Click on the **Player** sprite and add these blocks:
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Hazard v]?> then
>     broadcast [game over v]
>     go to x: () y: ()
>   end
> end
> ```

> [!TASK]
>
> If you want the player to start again, then add the new position into `go to x: y:`{:class="block3motion"}.

<h2 class="c-project-heading--task">Test</h2>

> [!TASK]
>
> Click the green flag and check that the `Hazard` moves and broadcasts `game over` on contact.
