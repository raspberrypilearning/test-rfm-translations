## 3B - Clone Platforms

Use one **Platform** sprite from an image or the Scratch library, then clone it to create all the platforms for your level.

## Step 1

> [!TASK]
>
> Choose a platform image or a Scratch sprite to use as your **Platform**.
>
> The place where the **Player** stands must have a straight, horizontal top.
>
> If you upload an image, crop away all the empty or transparent pixels around the platform before you upload it. The platform should fit tightly inside the image.
>
> Use an image you made yourself or have permission to use.

## Step 2

> [!TASK]
>
> Add your platform as a new sprite.
>
> To upload an image, open the **Choose a Sprite** menu and select the **Upload Sprite** icon.
>
> ![The Choose a Sprite menu.](images/choose_sprite.png)
>
> To use a Scratch sprite, open the **Choose a Sprite** menu and select **Choose a Sprite**.
>
> ![The Choose a Sprite option in the sprite menu.](images/sprite-choose.png)

## Step 3

> [!TASK]
>
> In the sprite pane, change the sprite name to **Platform**.
>
> Use this exact spelling so later steps can check whether the **Player** is touching the **Platform** sprite or any of its clones.
>
> You do not need separate sprites called `Platform1`, `Platform2`, or `Platform3`.

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
> Hide the original **Platform** sprite, move it to the front layer, and set its size.
>
> ```blocks3
> +when green flag clicked
> +hide
> +go to [front v] layer
> +set size to (100)%
> ```

## Step 6

> [!TASK]
>
> Add blocks to move the **Platform** sprite to the floor position and create a clone.
>
> Change the `x` and `y` values to match your own level.
>
> ```blocks3
> when green flag clicked
> hide
> go to [front v] layer
> set size to (100)%
> +go to x: (0) y: (-150)
> +create clone of [myself v]
> ```

## Step 7

> [!TASK]
>
> Add more `go to x: y:`{:class="block3motion"} and `create clone of [myself v]`{:class="block3control"} blocks for each extra platform.
>
> These clones are still part of the **Platform** sprite.
>
> ```blocks3
> when green flag clicked
> hide
> go to [front v] layer
> set size to (100)%
> go to x: (0) y: (-150)
> create clone of [myself v]
> +go to x: (-120) y: (-40)
> +create clone of [myself v]
> +go to x: (140) y: (20)
> +create clone of [myself v]
> ```

## Step 8

> [!TASK]
>
> Add a second script to the **Platform** sprite that starts when each clone is created.
>
> Make each clone show and go to the front layer.
>
> ```blocks3
> +when I start as a clone
> +show
> +go to [front v] layer
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the platform clones appear in the places you chose.
>
> The **Player** should be able to stand or jump on each platform clone.
