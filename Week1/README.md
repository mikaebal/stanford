<h1>Week 1</h1>

<h2>Jigsaw Karel</h2>

<b>Description: </b>Jigsaw Karel solves a maze, places the last beeper in the correct spot, and returns to the starting position.</b>
<br/><b>Code:</b>

```python

def main():
    """
    Karel organizes her world by putting a misplaced beeper perfectly back into its place within a puzzle of organized beepers.
    Karel then returns back to her original corner, pridefully admiring her accomplishment. 
    """
    move_to_beeper()
    place_beeper_correctly()
    return_to_start()
    
def move_to_beeper():
    """Moves Karel to the location of the beeper."""
    move()
    move()

def place_beeper_correctly():
    """Karel picks up the beeper and places it in the correct spot in the puzzle."""
    pick_beeper()
    move()
    turn_left()
    move()
    move()
    put_beeper()

def return_to_start():
    """Karel returns to the starting position."""
    turn_around()
    move()
    move()
    turn_right()
    move()
    move()
    move()
    turn_around()

def turn_around():
    """Turns Karel around by 180 degrees."""
    turn_left()
    turn_left()

def turn_right():
    """Turns Karel to the right."""
    turn_left()
    turn_left()
    turn_left()

if __name__ == '__main__':
    main()

```

<b>Result:</b>

![ezgif com-video-to-gif-converter (1)](https://github.com/user-attachments/assets/de9870d0-9af8-4316-9c61-789c8f9ab75a)

</br>

<h2>2023 Karel</h2>

<b>Description:</b> Karel places 20 and 23 beepers to create the year 2023 while ending facing East to the right of the 23 beepers.</b>

<b>Code:</b>

```python
def main():
    for i in range(20):
        put_beeper()
    move()
    for i in range(23): 
        put_beeper()
    move()
        
if __name__ == '__main__':
    main()
```

<b>Result:</b>

![ezgif com-video-to-gif-converter (2)](https://github.com/user-attachments/assets/9a524f54-36e9-4177-b7f6-689954f1c14a)

</br> 

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
