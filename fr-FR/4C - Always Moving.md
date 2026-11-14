## 4C - Always Moving

Make the **Player** keep moving, and use the arrow keys to change direction.

## Step 1

> [!TASK]
>
> Select the **Player** sprite in the sprite pane.

## Step 2

> [!TASK]
>
> Open the **Code** tab.
>
> ![The Code tab in Scratch.](images/tab_code.png)

The starter project already includes an `Up Down Helper` block, and the **Player** setup script with these **player** variables:

`x speed`{:class="block3variables"}, `y speed`{:class="block3variables"}, `gravity`{:class="block3variables"}, `jump strength`{:class="block3variables"}, `move speed`{:class="block3variables"}, `on ground`, `vertical steps`{:class="block3variables"}

## Step 3

> [!TASK]
>
> Add a block to set the sprite's speed and then use a `forever`{:class="block3control"} loop to start it moving
>
> ```blocks3
> when green flag clicked
> go to x: (100) y: (100)
> +set [x speed v] to (move speed)
> +forever
> change x by (x speed)
> end
> ```

## Step 4

> [!TASK]
>
> At the moment the sprite will alway move to the right. Add an `if`{:class="block3control"} block so that the sprite changes its speed and direction when the left key is pressed
>
> ```blocks3
> when green flag clicked
> go to x: (100) y: (100)
> set [x speed v] to (move speed) 
> forever
> +if <key (left arrow v) pressed?> then
> point in direction (-90)
> set [x speed v] to ((0)-(move speed))
> end
> change x by (x speed)
> end
> ```

## Step 5

> [!TASK]
>
> Add another `if`{:class="block3control"} block to change direction back again
>
> At the moment the sprite will alway move to the right. Add an `if`{:class="block3control"} block so that the sprite changes its speed and direction when the left key is pressed
>
> ```blocks3
> when green flag clicked
> go to x: (100) y: (100)
> set [x speed v] to (move speed) 
> forever
> if <key (left arrow v) pressed?> then
> point in direction (-90)
> set [x speed v] to ((0)-(move speed))
> end
> +if <key (right arrow v) pressed?> then
> point in direction (-90)
> set [x speed v] to (move speed)
> end
> change x by (x speed)
> end
> ```

## Test

> [!TASK]
>
> Click the green flag and check that the **Player** starts moving.
>
> Press the arrow keys to change direction.
>
> You can change the value of `move speed`{:class="block3variables"} if you want the sprite to move faster or slower.