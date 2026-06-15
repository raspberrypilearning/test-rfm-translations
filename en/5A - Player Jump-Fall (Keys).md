## 5A - Player Jump/Fall (Keys)

Make your **player** sprite jump.

## Step 1

> [!TASK]
>
> Select the **Player** sprite and find your movement blocks.

## Step 2

> [!TASK]
>
> Add in a new `if`{:class="block3control"} block, below the others, but above the `change x by ()`{:class="block3motion"} block.
>
> ```blocks3
> +if <> then
> end
> change x by (x speed)
> ```

## Step 3

> [!TASK]
>
> Detect space key presses in `if`{:class="block3control"} and then change the `y speed`{:class="block3variables"} of the **player**.
>
> ```blocks3
> +if <key (space v) pressed?> then
> set [y speed v] to (jump strength)
> end
> change x by (x speed)
> ```

## Test

> [!TASK]
>
> Click the green flag and press the space key to jump
>
> If you press the key several times, then the sprite will jump "double-jump".

## Step 4

> [!TASK]
>
> If you don't want to enable double-jumps, then jumping should only work when the sprite is on the ground. There's an `on ground`{:class="blocks3variables"} to detect this.
>
> ```blocks3
> + if <<key (space v) pressed?> and <(on ground) = (1)>> then
> set [y speed v] to (jump strength)
> end
> change x by (x speed)
> ```

## Test

> [!TASK]
>
> Click the green flag and press the space key several times. The **player** should only jump once.

## Step 5

> [!TASK]
>
> Change the height the **player** can jump and the speed that it falls, by changing the `gravity`{:class="block3variables"} and `jump strength`{:class="block3variables"} variables.
>
> ```blocks3
> set [gravity v] to (-1)
> set [jump strength v] to (15)
> ```


