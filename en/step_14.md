## 6A - Draw Exit Sprite

Draw your own **Exit** sprite to show where the player should finish the level.

## Step 1

> [!TASK]
>
> Open the **Sprite** menu and select **Paint**.
>
> ![The Paint option in the Choose a Sprite menu.](images/sprite-paint.png)

## Step 2

> [!TASK]
>
> Draw an exit object such as a door, portal, flag, treasure, or finish marker.
>
> Make it clear and easy to spot on your backdrop.

## Step 3

> [!TASK]
>
> In the sprite pane, change the sprite name to **Exit**. Use this exact spelling so later steps can refer to the same sprite.

## Step 4

> [!TASK]
>
> Select the **Exit** sprite and add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 5

> [!TASK]
>
> Add a `show` block below the green flag block.
>
> ```blocks3
> when green flag clicked
> +show
> ```

## Step 6

> [!TASK]
>
> Move the **Exit** sprite to where you want the door to be in the level.
>
> Drag it on the Stage so you can see the coordinates you want to use.

## Step 7

> [!TASK]
>
> Add a `go to x: () y: ()` block below `show`.
>
> Type the coordinates of the exit position into the white inputs to set its starting place.
>
> ```blocks3
> when green flag clicked
> show
> +go to x: () y: ()
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Exit** sprite appears where the player can reach it.
