## 3B - Make Platforms Move

Make a **Platform** sprite glide between two places to add timing and challenge.

## Step 1

> [!TASK]
>
> Open the **Choose a Sprite** menu and select **Paint**. Draw a simple rectangle, ledge, or stepping stone for the moving platform.
>
> If you already have a platform sprite, select it in the sprite pane.
>
> ![The Paint option in the Choose a Sprite menu.](images/sprite-paint.png)

## Step 2

> [!TASK]
>
> In the sprite pane, change the sprite name to **Platform**. Use this exact spelling so later steps can check whether the **Player** is touching it.

## Step 3

> [!TASK]
>
> Put the **Platform** sprite where you want it to start. Decide where it should glide to before returning.

## Step 4

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

## Step 5

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 6

> [!TASK]
>
> Add a block to show the **Platform** sprite.
>
> ```blocks3
> when green flag clicked
> +show
> ```

## Step 7

> [!TASK]
>
> Add a block to move the **Platform** sprite to its starting position.
>
> ```blocks3
> when green flag clicked
> show
> +go to x: () y: ()
> ```

## Step 8

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop below the starting position block.
>
> ```blocks3
> when green flag clicked
> show
> go to x: () y: ()
> +forever
> +end
> ```

## Step 9

> [!TASK]
>
> Inside the `forever`{:class="block3control"} loop, add a `glide`{:class="block3motion"} block for the place the **Platform** should move to.
>
> ```blocks3
> when green flag clicked
> show
> go to x: () y: ()
> forever
> +  glide () secs to x: () y: ()
> end
> ```

## Step 10

> [!TASK]
>
> Add a second `glide`{:class="block3motion"} block so the **Platform** returns to another place.
>
> ```blocks3
> when green flag clicked
> show
> go to x: () y: ()
> forever
>   glide () secs to x: () y: ()
> +  glide () secs to x: () y: ()
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Platform** sprite moves between the two places you chose.
