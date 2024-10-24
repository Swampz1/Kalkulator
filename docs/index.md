#Tutorial for beginners

##How To Make a Python Calculator

## Step One
### Choose a text editor
1. I like to use visual studio code as my text editor. You can download it [here](https://code.visualstudio.com/download). you can also use other text editors, such as PyCharm or others.
2. if you are using visual studio code, you can install the python extension.
3. if you are using other text editors, make sure you have python installed. [install](https://www.python.org/downloads/).

## Step Two
### Create a file

1. Create a new file in the text editor and call it main.py.
### Libraries
2. write the code below in the file:
```python
import tkinter as tk
from tkinter import ttk
```
tkinter is the standard Python library for building GUIs. It is imported as tk.

ttk is a submodule of tkinter that provides themed widgets like buttons, labels, and entry fields, giving a modern look to the application.

### Functions

3. Lets define our first function: 
```python
    def handle_button_click(clicked_button_text):
        current_text = result_var.get()
```
this function is the core function that handles the logic of the calulator when a button is clicked. for example, if the user clicks the 7 button, the function will return the text 7.

```python
expression = current_text.replace("÷", "/").replace("x", "*")
result = eval(expression)
```

This code is used to convert the text to a mathematical expression.

The eval function is used to evaluate the mathematical expression.

```python
 if result.is_integer():
                result = int(result)
```
This code checks if the result is an integer. If it is, it is converted to an integer.

```python
result_var.set(result)
        except Exception as e:
            result_var.set("Error")
    elif clicked_button_text == "C":
        result_var.set("")
    elif clicked_button_text == "%":
        try:
            current_number = float(current_text)
            result_var.set(current_number / 100)
        except ValueError:
            result_var.set("Error")
```	

This portion of the code is part of the handle_button_click() function, and it handles specific actions for different calculator buttons: the =, C, and % buttons.

```python
elif clicked_button_text == "±":
        try:
            current_number = float(current_text)
            result_var.set(-current_number)
        except ValueError:
            result_var.set("Error")
    else:
        result_var.set(current_text + clicked_button_text)
```

This portion of the code is also part of the handle_button_click() function, and it handles the ± button.
```python	
root = tk.Tk()
root.title("Calculator")

root.configure(bg="Black")

result_var = tk.StringVar()
result_entry = ttk.Entry(root, textvariable=result_var, font=("Helvetica", 24), justify="right")
result_entry.grid(row=0, column=0, columnspan=4, sticky="nsew")
```	
### Code Explanation for Documentation

`root = tk.Tk()`: Initializes the main application window for the calculator.

`root.title("Calculator")`: Sets the window's title to "Calculator".

`root.configure(bg="Black")`: Sets the background color of the window to black.

`result_var = tk.StringVar()`: Creates a string variable to store and update the text displayed in the calculator's result area.

`result_entry = ttk.Entry(root, textvariable=result_var, font=("Helvetica", 24), justify="right")`: Creates a text entry field (where results and expressions will be shown) with:
Large Helvetica font size (24) for better readability.
Right-aligned text, similar to typical calculator displays.

`result_entry.grid(row=0, column=0, columnspan=4, sticky="nsew")`: Positions the entry field at the top of the grid, spanning 4 columns and expanding to fit the available space. 

This section sets up the main window and the display area for the calculator.









