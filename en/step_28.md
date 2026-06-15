<h2 class="c-project-heading--task">10D - Add Enemies</h2>

Add an enemy hazard with a movement pattern that is different from simple left-right or up-down movement.

## Step 1

> [!TASK]
>
> Create a new sprite and name it **Enemy**.
>
> > [!TIP]
> >
> > You can download this blob enemy to use.
> > [![Enemy sprite example](images/enemy-blob.png){:width="300px"}](images/enemy-blob.png)

## Step 2

> [!TASK]
>
> Resize and place the **Enemy** sprite somewhere dangerous.
>
> Enemies are hazards, but they should feel more alive than spikes or lava. Put them on a platform, beside a gap, or near a place where the player needs careful timing.

## Step 3

> [!TASK]
>
> Choose a movement pattern for the **Enemy**.
>
> You could make it patrol around a small route, spin as it moves, or use uneven glide times so it feels less predictable than a simple moving hazard.

## Step 4

> [!TASK]
>
> Add this patrol script to the **Enemy** sprite.
>
> Type your own `x`{:class="block3motion"} and `y`{:class="block3motion"} positions for each place the enemy should visit.
>
> ```blocks3
> when green flag clicked
> go to x: () y: ()
> forever
>   glide () secs to x: () y: ()
>   glide () secs to x: () y: ()
>   glide () secs to x: () y: ()
> end
> ```

## Step 5

> [!TASK]
>
> If you want the enemy to spin while it patrols, add this second script to the **Enemy** sprite.
>
> ```blocks3
> when green flag clicked
> forever
>   turn cw (15) degrees
>   wait (0.05) seconds
> end
> ```

## Step 6

> [!TASK]
>
> Click on the **Player** sprite and add these blocks:
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Enemy v]?> then
>     broadcast [game over v]
>     go to x: () y: ()
>   end
> end
> ```

> [!TASK]
>
> If you want the player to start again, then add the new position into `go to x: y:`{:class="block3motion"}.

## Test

> [!TASK]
>
> Click the green flag and check that the **Enemy** follows its pattern and causes `game over` when touched.
