<h2 class="c-project-heading--task">10D - Add Enemies</h2>

Add an enemy hazard with a movement pattern that is different from simple left-right or up-down movement.

## Step 1

> [!TASK]
>
> Create a new sprite and name it **Enemy**.
>
> > [!TIP]
> >
> > You can download this blob enemy to upload, choose one from the Scatch library or draw your own:
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
> You could make it patrol around a small route, then spin before it moves again.

## Step 4

> [!TASK]
>
> Add this patrol and spin script to the **Enemy** sprite.
>
> Type your own `x`{:class="block3motion"} and `y`{:class="block3motion"} positions for each place the enemy should visit.
>
> The enemy spins between each glide. Each spin turns `36`{:class="block3motion"} degrees `10`{:class="block3control"} times. This makes `360` degrees, so the enemy is upright before it moves again.
>
> ```blocks3
> when green flag clicked
> go to x: () y: ()
> forever
>   glide () secs to x: () y: ()
>   repeat (10)
>     turn cw (36) degrees
>   end
>   glide () secs to x: () y: ()
>   repeat (10)
>     turn cw (36) degrees
>   end
>   glide () secs to x: () y: ()
>   repeat (10)
>     turn cw (36) degrees
>   end
> end
> ```
>
> To make it seem more random, make sure the **glide** times are all different, or `pick a random number`{:class="block3operators"}.

## Step 5

> [!TASK]
>
> Try changing the spin pattern.
>
> Make sure the repeat number multiplied by the turn angle equals `360`, such as `repeat 12` and `turn 30 degrees`, or `repeat 8` and `turn 45 degrees`.

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
