<h2 class="c-project-heading--task">9A - Static Hazard</h2>

Add spikes, lava or another non-moving hazard for the player to avoid.

## Step 1

> [!TASK]
>
> Create a new sprite and give it an obvious name like **Hazard** or **spikes**.
>
> > [!TIP]
> >
> > You can use download these spikes and use them in your game.
> > [![Spike hazard sprite](images/spikes.png){:width="300px"}](images/spikes.png)

## Step 2

> [!TASK] With a title
>
> In the **paint window**, resize and put your hazard where you want it, to make sure it fits on the level.

## Step 3

> [!TASK]
>
> Click your **Player** sprite, and add these blocks:
>
> ```blocks3
> when green flag clicked
> forever
>   if <touching [hazard v]?> then
>     set [x speed v] to (0)
>     set [y speed v] to (0)
>     go to x: () y: ()
>   end
> end
> ```

> [!TASK]
>
> Add the same position you used in the **Player** starting script into `go to x: y:`{:class="block3motion"}.
>
> This resets the **Player** instead of stopping the game.

## Test

> [!TASK]
>
> Touch the spikes and check that the **Player** goes back to the start position.

## Add More Hazards

> [!TASK]
>
> When your hazard works, right-click or long-press the **Hazard** sprite and choose **duplicate**.
>
> Drag the new hazard sprite to another place in your level.
>
> Repeat this to add spikes, lava, or other hazards around the level - you can even **add new costumes** for each, to add some variety to your game.
