## 3A - Add Floors and Platforms

Add a **Platform** sprite so the **Player** has somewhere to stand and jump.

## Step 1

> [!TASK]
>
> Open the **Choose a Sprite** menu and select **Paint**.
>
> ![The Paint option in the Choose a Sprite menu.](images/sprite-paint.png)

## Step 2

> [!TASK]
>
> Draw a wide rectangle for the floor. Add ledges or stepping stones if you want more places for the **Player** to land.
>
> Keep the shapes simple and clear. The platform needs to be easy to see against your backdrop.

## Step 3

> [!TASK]
>
> In the sprite pane, change the sprite name to **Platform**. Use this exact spelling so later steps can check whether the **Player** is touching it.

## Step 4

> [!TASK]
>
> Put the **Platform** sprite where the **Player** can reach it. Use the **Size** control if the platform is too large or too small.

## Step 5

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

## Step 6

> [!TASK]
>
> Add a script that starts when the green flag is clicked.
>
> ```blocks3
> +when green flag clicked
> ```

## Step 7

> [!TASK]
>
> Add a block to show the **Platform** sprite.
>
> ```blocks3
> when green flag clicked
> +show
> ```

## Step 8

> [!TASK]
>
> Add a block to move the **Platform** sprite to your chosen starting position.
>
> ```blocks3
> when green flag clicked
> show
> +go to x: () y: ()
> ```

## Step 9

> [!TASK]
>
> Add a block to set the **Platform** sprite's size.
>
> ```blocks3
> when green flag clicked
> show
> go to x: () y: ()
> +set size to ()%
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Platform** sprite appears where the **Player** can stand or jump to it.
