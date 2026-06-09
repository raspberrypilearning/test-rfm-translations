<h2 class="c-project-heading--task">9C - X-motion Hazards</h2>

Add a hazard that moves left and right to create danger.

## Step 1

> [!TASK]
>
> Create a new sprite for your hazard and give it a name such as **Hazard**.
>
> If you already made spikes or lava in `9A`, you can duplicate that sprite and use it here.

## Step 2

> [!TASK]
>
> Resize and place the **Hazard** sprite where you want it to start.
>
> Put it beside a platform, floor, or gap so it can move left and right across the player's path.

## Step 3

> [!TASK]
>
> Add these blocks to the **Hazard** sprite.
>
> Keep the two `y`{:class="block3motion"} positions the same. Change the two `x`{:class="block3motion"} positions to make the hazard move left and right.
>
> ```blocks3
> when green flag clicked
> go to x: () y: ()
> forever
>   glide () secs to x: () y: ()
>   glide () secs to x: () y: ()
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
> Click the green flag and check that the **Hazard** moves left and right and broadcasts `game over` on contact.
