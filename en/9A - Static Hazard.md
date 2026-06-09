<h2 class="c-project-heading--task">9A - Add Spikes</h2>

Add spikes for the player to avoid. 

## Step 1

> [!TASK]
>
> Create a new sprite and give it a name.
>
> > [!TIP]
> >
> > You can use download these spikes and use them in your game.
> > [![Spike hazard sprite](images/spikes.png)](images/spikes.png)

## Step 2

> [!TASK]
>
> In the **paint window**, resize and put your spikes where you want them.

## Step 3

> [!TASK]
>
> Click your **Player** sprite, and add these blocks:
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [Spikes v]?> then
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
> Touch the spikes and check that the `game over` message broadcasts.
