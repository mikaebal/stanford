<h1>Week 4</h1>

<h2>Khansole Academy</h2>

<b>Description:</b> A math practice program that quizzes the user on arithmetic problems, providing immediate feedback on their answers.</b>
<br/><b>Code:</b>

```python
import random

def main():
    print("Khansole Academy")
    
    num1 = random.randint(10, 99)
    num2 = random.randint(10, 99)
    total = num1 + num2 
    
    print("What is " + str(num1) + " + " + str(num2) + "?") 
    answer = int(input("Your answer: "))
    
    # True if answer is not equal to total
    if answer != total:
        print("Incorrect.")
        print("The expected answer is " + str(total)) 
    else:
        print("Correct!")
    
if __name__ == '__main__':
    main()
```

<b>Result:</b>
<p>
<img src="https://i.imgur.com/gz8iZBk.png" height="80%" width="80%" alt="Code Challenge Result"/>
</p>

</br>
 
<h2>Draw Flag</h2>

<b>Description:</b> A graphical program using python graphics that draws a flag of Indonesia on the screen.
<br/><b>Code:</b>

```python
from graphics import Canvas
import random

CANVAS_WIDTH = 450
CANVAS_HEIGHT = 300

def main():
    canvas = Canvas(CANVAS_WIDTH, CANVAS_HEIGHT)
    draw_indonesia_flag(canvas)
    
def draw_indonesia_flag(canvas):
    draw_rectangle(canvas, CANVAS_WIDTH, CANVAS_HEIGHT/2, 450, 'red')
    
    
def draw_rectangle(canvas, center_x, center_y, size, color):
    left_x = center_x - size
    top_y = center_y - size
    right_x = left_x + size
    bottom_y = top_y + size
    
    canvas.create_rectangle(left_x, top_y, right_x, bottom_y,'red')


if __name__ == '__main__':
    main()
```

<b>Result:</b>
<p>
<img src="https://i.imgur.com/52U6v0F.png" height="80%" width="80%" alt="Code Challenge Result"/>
</p>

