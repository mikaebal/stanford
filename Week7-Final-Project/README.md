<h1>🌟 Final Project</h1>

<h2>🗒️✍️ Interactive Notepad</h2>

<b>📝 Description:</b> For my final project, I developed an interactive digital notepad using the Canvas module. It features a styled border and lined paper, allowing users to draw by moving their mouse, which generates small circles to simulate pen strokes. The notepad smoothly tracks mouse movements, mimicking the experience of writing on paper.</b>

<p><b>👩🏻‍💻 Code:</b></p>

```python
from graphics import Canvas
import time

CANVAS_WIDTH = 400
CANVAS_HEIGHT = 400
SPACING = 20
CIRCLE_SIZE = 6
DELAY = 0.001

def main():
    canvas = Canvas(CANVAS_WIDTH, CANVAS_HEIGHT)

    # creating the notepad
    border = canvas.create_rectangle(49, 19, 351, 381, "black")
    notepad = canvas.create_rectangle(50, 20, 350, 380, "brown")
    pages = canvas.create_rectangle(50, 60, 350, 380, "yellow")
    red_line = canvas.create_line(100, 60, 100, 380, "red")

    # repeating lines on page
    current_y = 60
    while current_y <= 380:
        x = 50
        square = canvas.create_line(x, current_y, 350, current_y, "blue")
        current_y += SPACING

    # notepad title
    text = canvas.create_text(135, 25, font="American Typewriter", font_size=30, text='NOTEPAD')
    text = canvas.create_text(105, 65, font="American Typewriter", font_size=12, text='Start writing with your mouse!')

    # animation loop
    while True:
        # get the locations of the mouse
        mouse_x = canvas.get_mouse_x()
        mouse_y = canvas.get_mouse_y()

        # check that the mouse location is in bounds
        if mouse_x >= 50 and mouse_x <= 345 and mouse_y >= 60 and mouse_y <= 375:
            # draw a circle for where the mouse is
            canvas.create_oval(mouse_x, mouse_y, mouse_x + CIRCLE_SIZE, mouse_y + CIRCLE_SIZE, 'black')

        # animation loop code
        time.sleep(DELAY)

if __name__ == "__main__":
    main()
```

<b>✨ Result:</b>
    
![ezgif com-speed (1)](https://github.com/user-attachments/assets/29bc8436-ba6f-4719-8e64-e74c253f9534)
