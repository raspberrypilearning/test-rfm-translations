<h2 class="c-project-heading--task">9E - Add Enemies</h2>


Add an enemy that moves back and forth for the player to avoid.

## Step 1

> [!TASK]
>
> Create a new sprite and give it a name.
>
> > [!TIP]
> >
> > You can use download this blob enemy to use.
> > [![Enemy sprite example](images/enemy-blob.png)](images/enemy-blob.png)

## Step 2

> [!TASK]
>
> In the **paint window**, resize and put the **enemy** sprite on a platform or floor.

## Step 3

> [!TASK]
>
> Add these blocks to the **Enemy** sprite.
>
> Type `x`{:class="block3motion"} and `y`{:class="block3motion"} positions, and `glide`{:class="block3motion"} time.
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
>   if <touching [Enemy v]?> then
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
> Click the green flag and check that the `Enemy` patrols and causes `game over` when touched.
