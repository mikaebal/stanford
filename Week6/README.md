<h1>Week 6</h1>

<h2>Baby Snake</h2>

<b>Description:</b> A simple game where the user controls a snake that grows longer as it eats food.</b>
<br/><b>Code:</b>

```python
from graphics import Canvas
import time
import random

CANVAS_WIDTH = 400
CANVAS_HEIGHT = 400
VELOCITY = 20
SIZE = 20
# if you make this larger, the game will go slower
DELAY = 0.2

def main():
    canvas = Canvas(CANVAS_WIDTH, CANVAS_HEIGHT)
    start_x = 0  # Start at the top left corner
    start_y = 0
    score = 0
    direction = 'right'  # Initial direction

    # Place the goal at (360, 360)
    start_xx_goal = 360
    start_yy_goal = 360
    end_xx_goal = start_xx_goal + SIZE
    end_yy_goal = start_yy_goal + SIZE
    goal = canvas.create_rectangle(start_xx_goal, start_yy_goal, end_xx_goal, end_yy_goal, 'salmon')

    # create player
    player = canvas.create_rectangle(start_x, start_y, start_x + SIZE, start_y + SIZE, 'blue')

    # animation loop
    while True:
        # current player position
        curr_x = canvas.get_left_x(player)
        curr_y = canvas.get_top_y(player)

        key = canvas.get_last_key_press()
        if key == 'ArrowLeft' and direction != 'right':
            direction = 'left'
        elif key == 'ArrowRight' and direction != 'left':
            direction = 'right'
        elif key == 'ArrowUp' and direction != 'down':
            direction = 'up'
        elif key == 'ArrowDown' and direction != 'up':
            direction = 'down'

        # move the player based on the current direction
        if direction == 'left':
            start_x -= VELOCITY
        elif direction == 'right':
            start_x += VELOCITY
        elif direction == 'up':
            start_y -= VELOCITY
        elif direction == 'down':
            start_y += VELOCITY

        # update position of player
        canvas.move(player, start_x - curr_x, start_y - curr_y)

        # sleep
        time.sleep(DELAY)

        # detecting collisions
        if start_x < 0 or start_x >= CANVAS_WIDTH or start_y < 0 or start_y >= CANVAS_HEIGHT:
            canvas.clear()
            text = canvas.create_text(100, 150, text='Game Over! Try Again!', font_size=15)
            print('GAME OVER')
            break

        # check if player meets the goal
        if start_x == start_xx_goal and start_y == start_yy_goal:
            score += 1
            # moving the goal
            start_xx_goal = random.randint(0, CANVAS_WIDTH // SIZE) * SIZE
            start_yy_goal = random.randint(0, CANVAS_HEIGHT // SIZE) * SIZE
            canvas.delete(goal)  # Remove the previous goal
            goal = canvas.create_rectangle(start_xx_goal, start_yy_goal, start_xx_goal + SIZE, start_yy_goal + SIZE, 'salmon')

if __name__ == '__main__':
    main()
```
 [Demo](https://www.youtube.com)

