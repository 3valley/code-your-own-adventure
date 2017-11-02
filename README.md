**Table of Contents**

- [Code Your Own Adventure](#)
	- [Vocabulary list:](#)
		- [Program](#)
		- [Syntax](#)
		- [Comment](#)
		- [Variable](#)
		- [Data Types](#)
		- [Conditional statements:](#)
	- [Because it’s fun](#)
		- [input](#)
	- [A little trickier, but important!](#)
		- [function](#)
		- [control statements or loops](#)

# Code Your Own Adventure
Python is a high-level dynamic programming language commonly used for teaching, 
but it is by no means only for teaching… Instagram is written in Python, and YouTube used to be
I think it (and the community surrounding it) have a sort of friendly spirit. It is named after Monty Python’s Flying Circus, after all.

## Vocabulary list:
### Program
A **program** is a set of instructions that performs a task when executed (or **run**) by a computer.  
When using trinket.io, your program is in the left pane and the program’s output is on the right.

Try typing this at the top of the left pane  
```python
print 'hello world'
```
then click the Run button ▶

### Syntax
Like a human language, there are grammar and punctuation rules you must follow (although humans don’t usually grab you in the middle of a sentence, yell ERROR and refuse to let you continue talking until you use grammar correctly)

Trinket.io has **syntax highlighting**, where the things you type will change color based on what part of the code they represent. This can be useful for catching errors. (For example, a string without quote marks will be black instead of red)

### Comment
**Comments** have no effect on the program, so you can use them to describe the code (and write notes to yourself). You can also **comment out** chunks of your program by placing comments in front of existing code. This is useful for testing things and diagnosing problems.

Single-line comments start with a #  
```python
# Single-line comment
```

Multiple-line comments are wrapped in triple quotes  
```python
""" Multiline
	comment """
```
You can select text, then hit <kbd>control</kbd> + <kbd>/</kbd> to insert a single-line omment automatically

### Variable
A **variable** is a placeholder (I like to think of it as a little container, like a Tupperware) for a value. The contents of the variable can __vary__ as your program runs. Variables can have any name, as long as it starts with a letter or an underscore. No spaces allowed!

When you create a variable, you also **assign** a **value** to it by adding an equals sign `=` and then a value.
```python
tupperware = 'green beans'
```

Values can be different **data types**, each with their own syntax.

### Data Types
**Int:** A whole number (__int__ eger)  
```python
coins = 3
```

**Float:** Number with a decimal point (__float___ ing point)  
```python
temperature = 96.2
```

**String:** Text, always needs quotation marks around it `'like this'` or `"like this"`  
```python
greeting = "Welcome to Code Your Own Adventure"
```

**Boolean:** Holds only a true or false value. Must be written in caps, `True` or `False`  
```python
is_eaten = True
```

**List:** Called an array in other languages. Multiple items contained in one variable, surrounded by brackets with commas in between items. This is a list of strings:  
```python
backpack = ['map', 'flashlight']
```
Values in the list are **indexed** in the order you added them, so you can recall them by specifying the **index** number in brackets `[]`.  
`print backpack[1]` would display `flashlight`, because indexes start from `0`, not `1`

**Dictionary:**
Dictionaries are like lists, but instead of indexed values, they have **key-value pairs**. 

In this dictionary, the string `'sandwich'` is a **key** and the string `'baloney'` is the **value**: 
```python
Lunchbox = {'sandwich':'baloney', 'snack':'apple', 'dessert':'oreos'}
```

If I wanted to know what sandwich was in my lunchbox today, I could do:  
```python
print lunchbox['sandwich']
``` 
which would display `baloney`

### Conditional statements:
The main reason I chose adventure games as the theme of this class is because it gives you an excuse to use lots of **conditional statements**, also called an **`if` statement**, and `if` statements are fun to write.

Let's break down this `if` statement:  
```python
if lunchbox['sandwich'] == baloney:
	print 'My favorite!'
else:
	print 'Oh well, not my favorite sandwich'
```
  
`if` is followed by a **condition**; that is, a question that **evaluates** or compares two (or more) things and has either a `True` or `False` answer. 

The condition here is `lunchbox[‘sandwich’] == 'baloney'`, *"if the value paired with the key ‘sandwich’ in the dictionary ‘lunchbox’ is the same as 'baloney'"*

The symbol in the middle is called the **operator**. The operator here is `==`, *is equal to*

There are many operators and with them, options for writing conditions. Here are some others:  
```python
if 3 > 4
```
(*"if three is greater than four"*, evaluates to `False`)

```python
if len('pumpkin') >= 7
```
(*"if the length of the string ‘pumpkin’ is greater than or equal to seven"*, evaluates to `True`)  

After the condition, there’s a colon `:` to end the **header** of the statement.  
Any indented text after the colon will be the **body** of the statement.

The body is where you can add tasks that should only be performed if the condition is `True`
The body of my `if` statement is:
```python
	print 'My favorite!'
```
This code will only run if the value of `sandwich` is equal to `baloney`. __Otherwise, it will be skipped__. 

Things could end here, but I also have an `else` in this statement, with its own body where I can place a task. So I have two possible outcomes: one task for baloney, and a different task for every other sandwich.

Here is the body of the `else` statement:  
```python
	print 'Oh well, not my favorite sandwich'
```

Your `if` statement can have additional, optional parts. For example, I could add an `elif` (short for *else if*) followed by another condition to my statement (with an additional task in the body of the `elif` statemet) to handle a second sandwich option, and then an `else` as a catchall for any other kind of sandwich (one that isn’t the same as baloney AND isn’t the same as chicken salad)

```python
if lunchbox['sandwich'] == ‘baloney’:
	print 'My favorite!'
elif lunchbox['sandwich'] == 'chicken salad':
	print 'My second favorite!'
else:
	print 'Oh well, not any of my favorite sandwiches'
```

An `if` statement always starts with `if` 
Optionally, you can add as many `elif`s as you like
Optionally, you can add an `else` as a catchall for everything that wasn’t caught by `if` and/or `elif`

## Because it’s fun
### input
You can use the built-in `input()` feature to get input from the user:   
```python
their_sandwich = input('What\'s your favorite sandwich?')
```
Your program will pause and wait for the user to enter something via the keyboard.

Here, I am assigning the user’s response to a variable, `their_sandwich`, so I can do something with it- for example, use it in an `if` statement:  
```python
if their_sandwich == lunchbox['sandwich']:
	print "Wow, we have the same favorite sandwich"
else:
	print "Never heard of it"
 ```

## A little trickier, but important!
### function
**Functions** are a little package of code that performs a task.  
I think of them as a machine in a factory.   
Python has some functions built in. We briefly saw `len()`, for example.  

You can (and should!) write your own functions, though!

Here are the parts of a function:
```python
def fruit_slicer(fruit):
	fruit = fruit + " slices"
  	return fruit
```

First, we **declare** that we are going to make, or **define**, a function by writing `def`  
`fruit_slicer` is the name of the function  
The parentheses are where we put a **parameter**, which is a placeholder for the real value we will eventually use. In this case, `fruit` is the parameter. The colon `:` is the end of the function heading. Any indented text after the colon will be inside the body of the function.

We’re going to do a (silly) task to anything that comes inside the function- we’re going to add the word `" slices"` to it. Again, the parameter `fruit` is just a placeholder for whatever gets fed in there.

`return` spits the finished product out of the function.

Now, we call the function by name, and put the thing we want sliced between the parentheses- the **argument**. So the string `‘apple’` is the argument this time:
```python
print fruit_slicer('apple')
```

### control statements or loops
Right now, your program is running from top to bottom until it runs out, and then it sits there until you run it again.
If there’s anything computers are really good at, it’s doing stuff over and over really fast. So when you want to do something a lot of times, let the computer do the hard work by using a control statement to make a **loop**. 

If I wanted to slice three apples, I could do:
```python
print fruit_slicer(‘apple’)
print fruit_slicer(‘apple’)
print fruit_slicer(‘apple’)
```

Or I could use a `for` loop

```python
for apples in range(3):
	print fruit_slicer('apple')
```

It begins with `for`  
`apples` is just a placeholder, and the built-in function `range()` lets use choose how many times the loop should go around (in this case, `3`). So we’re saying *"for as many things as there are in a range of three… do the task inside the loop"*

`for` loops get really handy when we’ve got a list of something and we want to do a task to every item in the list.

First I made a nice list of fruit, then I feed my variable `fruit_basket` into the `fruit_slicer` function:
```python
fruit_basket = ['apple', 'orange', 'peach', 'pear']

for fruit in fruit_basket:
	print fruit_slicer(fruit)
```

Like in the previous loop, the word `fruit` is just a placeholder that I gave a compelling name. `fruit_basket` is the name of that variable.

Now my `for` loop reads *"For as many fruit as there are in the variable fruit_basket, call fruit_slicer on each individual fruit, in order, until there are no more."*
