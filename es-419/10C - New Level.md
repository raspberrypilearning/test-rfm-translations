<h2 class="c-project-heading--task">10C - Nuevo Nivel</h2>

Crea un segundo diseño de plataforma y cambia a él cuando el jugador cumpla la condición de victoria.

## Paso 1

> [!TASK]
>
> Selecciona tu sprite de **Plataforma** en el panel de sprites.
>
> Abre la pestaña **Disfraces**.

## Step 2

> [!TASK]
>
> Rename the costume for your current platform layout to `level 1`.
>
> Si dibujaste o subiste tus plataformas anteriormente, usa el disfraz que ya coincida con tu primer nivel.

## Step 3

> [!TASK]
>
> Duplicate the `level 1` costume and rename the copy `level 2`.
>
> This gives you a second platform costume that you can edit without changing the first level.

## Step 4

> [!TASK]
>
> Edit the `level 2` costume to create a new platform layout.
>
> Keep the top edges straight and horizontal where the **Player** needs to stand.
>
> If you used hidden platform lines in `Add platforms to match your backdrop`, make the lines visible while you edit, then make them transparent again when you are finished.

## Step 5

> [!TASK]
>
> If you used `3A - Add platforms to match your backdrop`, select the **Stage** and create a matching second backdrop.
>
> Rename your current backdrop `level 1`, duplicate it, rename the copy `level 2`, and edit it so it matches the new platform layout.
>
> If you used `Draw foreground platforms` or `Draw Platforms in another editor`, you can skip this step.

## Step 6

> [!TASK]
>
> Open the **Code** tab.
>
> In the green flag script for the **Platform** sprite, add `switch costume to [level 1 v]`{:class="block3looks"}.
>
> Keep any other setup blocks you already use, such as `show`{:class="block3looks"}, `go to [front v] layer`{:class="block3looks"}, `go to x: (0) y: (0)`{:class="block3motion"}, or `set size to (100)%`{:class="block3looks"}.
>
> ```blocks3
> when green flag clicked
> switch costume to [level 1 v]
> show
> ```

## Step 7

> [!TASK]
>
> Add a new script that changes the **Platform** sprite to the second layout:
>
> ```blocks3
> when I receive [level 2 v]
> switch costume to [level 2 v]
> ```

## Step 8

> [!TASK]
>
> If you made a `level 2` backdrop, add these scripts to the **Stage**:
>
> ```blocks3
> when green flag clicked
> switch backdrop to [level 1 v]
>
> when I receive [level 2 v]
> switch backdrop to [level 2 v]
> ```

## Step 9

> [!TASK]
>
> Find the script from your win condition route.
>
> Change the `broadcast win`{:class="block3events"} block to `broadcast [level 2 v]`{:class="block3events"}.
>
> ```blocks3
> broadcast [level 2 v]
> ```

## Test

> [!TASK]
>
> Click the green flag and check that your first platform layout appears.
>
> Meet your win condition and check that the `level 2` message broadcasts and switches the **Platform** sprite to the second layout.
>
> If you made a second backdrop for `3A`, check that the **Stage** also switches to the `level 2` backdrop.
