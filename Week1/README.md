<h1>Week 1</h1>

<h2>Jigsaw Karel</h2>

<b>Description:</b> Jigsaw Karel solves a maze by following a set of predefined rules.</b>
<br/><b>Code:</b>

```python
def solve_maze():
    while front_is_clear():
        move()
    turn_left()
    while right_is_clear():
        turn_right()
        move()
        if right_is_clear():
            turn_right()
            move()
        else:
            turn_left()
    # Additional code logic here
```

<b>Result:</b>

https://github.com/user-attachments/assets/5839239d-5694-4c22-ae75-7aa6f427d64f

<br/>
 
<h2>Stone Mason Karel</h2>

<b>Description:</b>Stone Mason Karel rebuilds a series of columns along a path.
<br/><b>Code:</b>

```python
def rebuild_columns():
    while front_is_clear():
        repair_column()
        move_to_next_column()
    # Additional code logic here

def repair_column():
    turn_left()
    while front_is_clear():
        put_beeper()
        move()
    turn_around()
    move_to_wall()
    turn_left()

def move_to_next_column():
    for i in range(4):
        if front_is_clear():
            move()

def turn_right():
    for i in range(3):
        turn_left()

def turn_around():
    turn_left()
    turn_left()

def move_to_wall():
    while front_is_clear():
        move()
```
<b>Result:</b>

![ezgif-7-225fb41a8b](https://github.com/user-attachments/assets/98a5a6a4-53c9-4cd8-b4d9-c14f11d55e8a)


 
