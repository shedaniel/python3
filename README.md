# Python 3
This is a full tutorial on python.

### Print
Let's start with printing:
```python
print("Hello World!")
```
As you can see, there isn't any semicolons. The output of this code will be:
`Hello World!\n`

If you wonder how do you force remove the `\n`, what you can do is this:
```python
print("Hello World!", end="")
```
This set the value of `end` to `""`, which the default of `end` is `\n`. With the above code, python will output: `Hello World!`
#### Ways to print multiple objects
There are two ways to add multiple objects to the print function, the first one being this:
```python
print("Hello, I am", "Daniel")
```
For the above code, python with print out `Hello, I am Daniel\n`, you might notice the fact that python auto adds spaces between objects, but you can disable it by setting `sep` to `""`, demonstrated here:
```python
print("Hello, I am", "Daniel", sep="")
```
The method of using comma works with objects other than str too, like this:
```python
print("abc", 123)
```
The above code will print out `abc 123\n`.

The other way to add multiple objects is to use `+`, as shown here:
```python
print("ABC" + "DEF")
```
From the above code, python will output: `ABCDEF\n`, you will notice the absence of automatic space between ABC and DEF, as python treat `"ABC" + "DEF"` as a string instead of 2 strings, the flaw of this method is the lack of support for other types, such as this:
```python
print("I am " + 12 + " years old")
```
The above code should return an error as python can't add the strings and integer to 1 single string. The way to fix this is to cast `12` into a string:
```python
print("I am " + str(12) + " years old")
```

### Variables
Python's variables are dynamic, which means that you can change its type whenever you want. Declaring a variable is easy, shown here:
```python
a = 10
b = "abc"
c = 0.213
```
Unlike other languages, as its variables are dynamic, you can change its type:
```python
a = 10
a = "abc"
```
The above code will run without any error.

### Lists & Arrays
```python
a = []
```
Using the above code will create a list named a.
You can use lots of built-in methods to access it:
```python
a = []
a.append("abc")
a.pop(0)
```
The append method adds the object at the last index.
The pop method removes the object at a certain index.

You can get an item from the list by: `a[index]`. <br>
You can print the whole list by: `print(a)`, or just one value by `print(a[index])`

### Conditions
Conditions in python is pretty easy.
Python supports the usual logical conditions from mathematics:

    Equals: a == b
    Not Equals: a != b
    Less than: a < b
    Less than or equal to: a <= b
    Greater than: a > b
    Greater than or equal to: a >= b
Some examples here:
```python
a = 10
b = 20
if a < b:
    print("Yes")
elif a == b:
    print("Maybe")
else:
    print("Oh no!")
```
The above code prints out `Yes\n`
Python relies on indentation, using whitespace, to define scope in the code. Other programming languages often use curly-brackets for this purpose.
```python
a = 10
b = 20
if a < b:
print("Yes")
```
This above code will throw an error as it has not been indented correctly.
#### One line Conditions
If you have only one statement to execute, you can put it on the same line as the if statement.
```python
if a > b: print("a is greater than b")
```
If you have only one statement to execute, one for if, and one for else, you can put it all on the same line:
```python
print("A") if a > b else print("B") 
```
The above code is like `print(a > b ? "A" : "B")` in Java.

#### And
The `and` keyword is a logical operator, and is used to combine conditional statements:
```python
if a > b and c > a:
  print("Both conditions are True")
```

#### Or
The `or` keyword is a logical operator, and is used to combine conditional statements:
```python
if a > b or a > c:
  print("At least one of the conditions are True")
```

### Casting
There may be times when you want to specify a type on to a variable. This can be done with casting. Python is an object-orientated language, and as such it uses classes to define data types, including its primitive types.

Casting in python is therefore done using constructor functions:

    int() - constructs an integer number from an integer literal, a float literal (by rounding down to the previous whole number), or a string literal (providing the string represents a whole number)
    float() - constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)
    str() - constructs a string from a wide variety of data types, including strings, integer literals and float literals
For example for `int()`:
```python
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
```
For example for `float()`:
```python
x = float(1)     # x will be 1.0
y = float(2.8)   # y will be 2.8
z = float("3")   # z will be 3.0
w = float("4.2") # w will be 4.2
```
For example for `str()`:
```python
x = str("s1") # x will be 's1'
y = str(2)    # y will be '2'
z = str(3.0)  # z will be '3.0' 
```
