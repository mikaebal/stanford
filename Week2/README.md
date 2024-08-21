<h1>Week 2</h1>

<h2>Fill Karel</h2>

<b>Description:</b> Karel fills all empty spaces on the grid by placing beepers in every unoccupied spot.</b>
<br/><b>Code:</b>

```python
from karel.stanfordkarel import *

def main():
    put_beeper()
    while left_is_clear():
        fill_line()
        if front_is_blocked():
            reset_position()
    while front_is_clear():
        move()
        put_beeper()

def fill_line():
    while front_is_clear():
        move()
        put_beeper()

def reset_position():
    turn_around()
    while front_is_clear():
        move()
    turn_right()
    move()
    turn_right()
    put_beeper()

def turn_around():
    turn_left()
    turn_left()

def turn_right():
    for i in range(3):
        turn_left()

if __name__ == '__main__':

```

<b>Result:</b>

![CIPFillKarel-ezgif com-speed](https://github.com/user-attachments/assets/4300f126-a515-4f43-b4e1-c6c83aaf5c98)

 
<h2>Hello Name</h2>

<b>Description:</b> A program that prompts the user for their name and greets them with a personalized message.
<br/><b>Code:</b>

```python
def main():
    """
    You should write your code here. Make sure to delete 
    the 'pass' line before starting to write your own code.
    """
    name = input("What is your name? ")
    print("Hello", name)
    
if __name__ == '__main__':
    main()
```

 <b>Result:</b>

 https://github.com/user-attachments/assets/eefbe3db-7973-4965-83cb-3894ff010ae1

 
