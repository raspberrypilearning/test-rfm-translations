<h2 class="c-project-heading--task">10C - Change Level</h2>

Change the **Platform** sprite when the player wins, so the stage looks like a new level or end screen.

## Step 1

> [!TASK]
>
> Select the **Platform** sprite in the sprite pane.
>
> This is the same sprite you made in `3A - Draw Platforms` or `3B - Clone Platforms`.

## Step 2

> [!TASK]
>
> Open the **Costumes** tab.
>
> Duplicate the costume you already use for your platforms.
>
> Rename the first costume `level 1` and rename the new costume `level 2`.

## Step 3

> [!TASK]
>
> Edit the `level 2` costume to make a new level, end screen, or changed platform layout.
>
> If you drew one big **Platform** costume in `3A`, draw new floor and platform lines on `level 2`.
>
> If you used cloned platforms in `3B`, edit the `level 2` costume so each clone changes appearance when the level changes.

## Step 4

> [!TASK]
>
> Open the **Code** tab.
>
> Add this block to the **Platform** sprite's green flag script so the game always starts on `level 1`.
>
> ```blocks3
> when green flag clicked
> switch costume to [level 1 v]
> ```
>
> If the **Platform** sprite already has a green flag script, add the `switch costume to level 1` block near the top of that script.

## Step 5

> [!TASK]
>
> Add this script to the **Platform** sprite.
>
> When any win condition broadcasts `win`, the **Platform** sprite changes to the `level 2` costume.
>
> ```blocks3
> when I receive [win v]
> switch costume to [level 2 v]
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Platform** sprite starts with the `level 1` costume.
>
> Meet your win condition and check that the **Platform** sprite switches to the `level 2` costume when the `win` message broadcasts.
