<h1>Week 3</h1>

<h2>Mad Libs</h2>

<b>Description:</b> A program that asks the user for words to complete a story template, generating a fun, customized story based on their input.</b>
<br/><b>Code:</b>

```python
"""
Uses constants to tell a mad libs story.
"""

# Fun fact: 6174 is known as Kaprekar's constant,
# and it's a pretty mysterious number :)

WIZARD = 'Karel'
NUMBER_OF_FRUIT = 6174
FRUIT = 'mangoes'

def main():
    print("There once was a wizard by the name of " + WIZARD + " who loved to eat " + FRUIT + ".")
    print(WIZARD + " always kept a stash of " + str(NUMBER_OF_FRUIT) + " " + FRUIT + " in their house...")

if __name__ == '__main__':
    main()
```
 [Demo](https://www.youtube.com)
 
<h2>Multiply Two Numbers</h2>

<b>Description:</b>A program that takes two numbers as input and returns their product.
<br/><b>Code:</b>

```python
"""
Program: multiply two numbers
--------------------
This program asks the user for two
integers and prints the value of the first number
multiplied with the second
"""

def main():
    
    print("This program multiplies two numbers.")
    num1 = input("Enter first number: ")
    num1 = int(num1)
    num2 = input("Enter second number: ")
    num2 = int(num2)
    total = num1 * num2
    print(str(total))

# This provided line is required at the end of
# Python file to call the main() function.
if __name__ == '__main__':
    main()
```
 [Demo](https://www.youtube.com)

<h2>Joke Bot</h2>

<b>Description:</b>A simple program that displays a random joke for the user's entertainment.
<br/><b>Code:</b>

```python
PROMPT = "What do you want? "
JOKE = "Here is a joke for you! Karel is heading out to the grocery store. A programmer tells her: get a liter of milk, and if they have eggs, get 12. Karel returns with 13 liters of milk. The programmer asks why and Karel replies: 'because they had eggs'"
SORRY = "Sorry I only tell jokes"

def main():
    user_input = input(PROMPT)
    if user_input == "Joke":
        print(JOKE)
    else: 
        print(SORRY)
 
if __name__ == "__main__":
    main()
```
 [Demo](https://www.youtube.com)


 <h2>Double It</h2>

<b>Description:</b>A program that takes a number as input and returns double its value.
<br/><b>Code:</b>

```python
def main():
    # this program doubles the entered number until the value is greater than 100 
    curr_value = int(input("Enter a number: "))
    
    # display "invalid number" if the number entered is greater than 100 
    if curr_value > 100:
        print("Invalid number!")
        
    # if code block above is false and less than 100, the number will be doubled until the value is greater than 100
    else:
        while curr_value < 100:
            # Multiplies entered number by 2 
            print(curr_value * 2)
            # Doubles the current value 
            curr_value = curr_value * 2
    
if __name__ == '__main__':
    main()
```
 [Demo](https://www.youtube.com)
 
