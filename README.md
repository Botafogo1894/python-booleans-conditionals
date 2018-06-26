
# Booleans, Operators & Conditionals

Boolean values are generally `True` and `False` in Python. In fact, boolean values are used heavily in programming languages since they all eventually compile to binary code -- like in the matrix.

![matrix](matrix_binary.png)

Binary code is just `0`s and `1`s, On and Off, Yes and No, or *True* and *False*. 

In Python as with many other languages, there are things that are not purely `True` or `False`, but their value can be treated as `True` or `False`. We call these ***Truthy*** and ***Falsy***. So, while the value of the number `1` is not specifically `True`, it is Truthy (as are all other positive and negative intergers). Conversely, while the value of the number `0` is not specifically `False`, it is Falsy. We can test this with the `bool` operator, which returns to us the Boolean value of something (i.e. a truthy element returns True and a Falsy element returns False).

## bool() operator


```python
# testing truthiness and falsiness
print('1.', bool(True)) # True
print('2.', bool(False)) # False
print('3.', bool(1)) # True 
print('4.', bool(0)) # False
```

    1. True
    2. False
    3. True
    4. False



```python
# less obvious examples
print('1.', bool("hello")) # string 'hello' - True
print('2.', bool([])) # empty list - False
print('3.', bool(-300)) # negative number - True
print('4.', bool("")) # empty string - False
```

    1. True
    2. False
    3. True
    4. False


Here is a list of all the falsy values in Python:

*for now, the bolded examples are most important*
* **None**
* **False**
* **zero** of any numeric type, for example, **0**, 0L, **0.0**, 0j.
* **any empty sequence**, for example, **'', (), []**.
* **any empty mapping or dictionary**, for example, **{}**.
* instances of user-defined classes, if the class defines a `__nonzero__()` or `__len__()` method, when that method returns the integer zero or bool value False.

A list of all falsy values and more information on Booleans in Python can be found [here]('https://docs.python.org/2/library/stdtypes.html').

## Other things that return Boolean values - Comparison Operators

Comparison operators have a return value that is either True or False. In Python, comparison operators are:
```python
== # tests equality between two elements
!= # tests inequality between two elements
<, >, <=, >= # each tests the value between two elements
```
Perhaps the last line's operators are a little more familiar because we've seen these operators in math classes. But the first two might be bit more confusing, so, let's dive into those first.

The double equals operator (==) is testing whether the value of element1 is equal to that of element2.
```python 
False == True # returns False
False == False # returns True
10 == 20 # returns False
10 == 10 # returns True
"hi" == "HI" # returns False
"heLLo" == "heLLo" # returns True
```

The bang equals operator (!=) is testing whether the value of element1 is **not** equal to that of element2.

```python 
True != True # returns False
True != False # returns True
10 != 20 # returns True
10 != 10 # returns False
"hi" != "HI" # returns True
"heLLo" != "heLLo" # returns False
```




```python
print('1.', True != True) # False
print('2.', False == True) # False
print('3.', 10 == 10) # True
print('4.', "hi" == "HI") # False
print('5.', type(0) == int) # True
print('6.', ["hi"] == ["hi"]) # True
```

    1. False
    2. False
    3. True
    4. False
    5. True
    6. True

