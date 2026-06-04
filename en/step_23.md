<h2 class="c-project-heading--task">9C - Add Obstacles</h2>

Create barriers, blocks, crates, walls, or other objects that block the player or make the route more difficult.

## Step 1

> [!TASK]
>
> Create a new sprite and give it a name.

## Step 2

> [!TASK]
>
> Place the **obstacle** sprite where it makes the path more interesting. Obstacles should change movement, not automatically cause a loss.

## Step 3

> [!TASK]
>
> Click on your **player** sprite and add these blocks:
>
> ```blocks3
> when green flag clicked
> forever
>  if <touching [Obstacle v]?> then
>    change x by ((0) - (move speed))
>  end
> ```

<h2 class="c-project-heading--task">Test</h2>

> [!TASK]
>
> Move your player into an **obstacle** and check that it blocks or pushes back the player.
