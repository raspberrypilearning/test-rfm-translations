<h2 class="c-project-heading--task">10B - Add Sound effects</h2>

Add sound effects to make moments such as jumping, collecting items, winning, or danger feel more realistic.

## Step 1

> [!TASK]
>
> Click the sprite you want to add a sound effect to.

## Step 2

> [!TASK]
>
> Select the **Sounds** tab and then **Choose a Sound**.

## Step 3

> [!TASK]
>
> Choose a sound effect from the library.

## Step 4

> [!TASK]
>
> Add a sound to the collectable script so it plays when the player touches it. Use the same example script from 8B and add a `play sound [effect v] until done`{:class="block3sounds"} block:
>
> ```blocks3
> when green flag clicked
> show
> forever
> 	if <touching [Player v]?> then
> 		change [Score v] by (1)
> 		play sound [effect v] until done
> 		hide
> 	end
> end
> ```

> [!TIP]
>
> `play sound ... until done`{:class="block3sounds"} waits for the sound to finish before continuing, while `start sound ...`{:class="block3sounds"} plays the sound in the background and continues following the code immediately.

## Test

> [!TASK]
>
> Click the green flag and check that the sound works.
