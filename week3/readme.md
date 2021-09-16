# Week3

## Week 3 Topics
- Making Choices/Flow Control/Conditionals
- Data Structures (lists, tuples)
- Repeating code using loops

## Making Choices/Flow Control/Conditionals

- So far we have only written small programs that are a sequence of instructions. Sometimes you have to alter the sequential flow of a program to suit the needs of a particular situation.
- When strings are compared, they are compared lexicographic, meaning strings are put into alphabetical order and uppercase comes before lowercase.
- The conditional operator converts the conditional into a boolean, which is a basic Python data type.
- `bool` datatype only has two values: `True` or `False`
- There are only three Boolean operators: `and`, `or`, and `not`.

### Truthiness and Falsiness 
- Things that are false on their own
	- `None` (basic data type)
	- `False` (basic data type)
	- Any empty sequence: `''`, `[]`, `()`
	- Any zero value: 0, 0.0
	- Anything whose `len()` returns 0
	- Empty objects
	- Everything else is True 
	  

### Boolean Algebra

### Comparison (Relational) Operators
- Assume `a=1` and `b=1`

| Relational Operators | What it does?                                | Example       |
|----|---------------------------------------------|---------------|
| == | True if a has the same value as b           | a == b #True  |
| != | True if a does not have the same value as b | a != b #False |
| >  | True if a is greater than b                 | a > b # False |
| <  | True if a is less than b                    | a < b # False |
| >= | True if a is greater than or equal to b     | a >= b # True |
| <= | True if a is less than or equal to b        | a <= b # True |

### Logical Operators

| Operator | What it does?                                        | Example                                                                   |
|----------|------------------------------------------------------|---------------------------------------------------------------------------|
| `and`    | True if both a AND b are true (logical conjunction)  | if is_teacher and is_active:   print('You can access')                    |
| `or`     | True if either a OR b are true (logical disjunction) | if is_superuser or (is_teacher and is active):    print('You can access') |
| `not`    | True if the opposite of a is true (logical negation) | if not is_superuser:   print('You cannot access')    

`and` - both sides should be `True`

| x     | y     | x and y |
|-------|-------|---------|
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

`or` - at leas one side should be `True`

| x     | y     | x or y |
|-------|-------|---------|
| True  | True  | True    |
| True  | False | True   |
| False | True  | True   |
| False | False | False   |

`not` - change to opposite

| x     | not x |
|-------|-------|
| True  | False  |
| False | True  |

### Operator-Precedence
[Python documentation on operator-precedence](https://docs.python.org/3/reference/expressions.html#operator-precedence)


| Operator                                                              | Description                                                                        |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| (expressions...), [expressions...], {key: value...}, {expressions...} | Binding or parenthesized expression, list display, dictionary display, set display |
| x[index], x[index:index], x(arguments...), x.attribute                | Subscription, slicing, call, attribute reference                                   |
| await x                                                               | Await expression                                                                   |
| **                                                                    | Exponentiation 5                                                                   |
| +x, -x, ~x                                                            | Positive, negative, bitwise NOT                                                    |
| *, @, /, //, %                                                        | Multiplication, matrix multiplication, division, floor division, remainder 6       |
| +, -                                                                  | Addition and subtraction                                                           |
| <<, >>                                                                | Shifts                                                                             |
| &                                                                     | Bitwise AND                                                                        |
| ^                                                                     | Bitwise XOR                                                                        |
| \|                                                                    | Bitwise OR                                                                         |
| in, not in, is, is not, <, <=, >, >=, !=, ==                          | Comparisons, including membership tests and identity tests                         |
| not x                                                                 | Boolean NOT                                                                        |
| and                                                                   | Boolean AND                                                                        |
| or                                                                    | Boolean OR                                                                         |
| if – else                                                             | Conditional expression                                                             |
| lambda                                                                | Lambda expression                                                                  |
| :=                                                                    | Assignment expression                                                              |

### Examples
```python

not True
not False

True and True
False and False
True and False
False and True


True or True
False or False
True or False
False or True

```


```python
cold = True
windy = False

(not cold) and windy # It is not cold and windy

not (cold and windy) # 


```


### Relational Operators
- `==` Equal to 
- `!=` Not equal to
- `<` Less than
- `>` Greater than
- `<=` Less than or equal to
- `>=` Greater than or equal to

- These operators evaluate to True or False depending on the values you give them.
- Conditionals are used to instruct computer to make a decision. 

```python
45 > 34
45 > 79
45 < 79
45 < 34

23.1 >= 23
23.1 >= 23.1
23.1 <= 23.1
23.1 <= 23

67.3 == 87
67.3 == 67
67.0 == 67
67.0 != 67
67.0 != 23

```
###  Combining Comparisons

```python
x = 2
y = 5
z = 7
x < y and y < z

(x < y) and (y < z) # better

```

```python
x = 3
(1 < x) and (x <= 5)

x = 7
(1 < x) and (x <= 5)


x = 3 
1 < x <= 5 # You can chain comparisons

3 < 5 != True 
(3 < 5) and (5 != True)

3 < 5 != False
(3 < 5) and (5 != False)
```

### String Comparisons
```python
'A' < 'a'
'A' > 'Z'
'abc' < 'abd'
'abc' < 'abcd' # shorter is less

```

```python
'Jan' in '01 Jan 1838'

'Feb' in '01 Jan 1838'

'a' in 'abc'

'A' in 'abc'

```



### Choosing which statements to execute
[https://docs.python.org/3/reference/compound_stmts.html#if](https://docs.python.org/3/reference/compound_stmts.html#if)
#### If Statement

```Python
if Expression1:
    # Expression1 is True
    do_something_1
    do_something_else_1
```
#### If ... else ... Statement
```Python
if Expression1:
    # Expression1 is True
    do_something_1
    do_something_else_1
else:
    # Expression1 is False
    do_something_2
    do_something_else_2
```
#### If ... elif ... else ... Statement

```Python
if Expression1:
    # Expression1 is True
    do_something_1
    do_something_else_1
elif Expression2: # else if 
    # Expression2 is True and Expression1 is False
    do_something_2
    do_something_else_2
elif Expression3: # else if 
    # Expression3 is True and Expression1 and Expression2 are False
    do_something_3
    do_something_else_3
else:
    # Expression1, Expression2 and Expression3 are False
    do_something_4
    do_something_else_4
```
- colons are important and indentation matters
- can have many elif tests
- do not need else
- conditions can be nested



#### Example
| pH Level | Solution Category |
|----------|-------------------|
| 0-4      | Strong acid       |
| 5-6      | Weak acid         |
| 7        | Neutral           |
| 8-9      | Weak base         |
| 10-14    | Strong base       |

```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	print(ph, " is acidic.") #indentation important
```

```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	print(ph, " is acidic.")
	print('You should be careful with that!') #indentation is important
```


```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	print(ph, " is acidic.") #indentation important

if ph > 7.0:
	print(ph, " is basic.") 
```

```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	print(ph, " is acidic.") #indentation important
elif ph > 7.0:
	print(ph, " is basic.") 
```

```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	ph = 8.0 #indentation important

if ph > 7.0:
	print(ph, " is basic.") 
```


```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	ph = 8.0  #indentation important
elif ph > 7.0:
	print(ph, " is basic.") 
```


```python
ph = float(input('Enter the pH level: '))
if ph < 7.0:
	ph = 8.0  #indentation important
elif ph > 7.0:
	print(ph, " is basic.") 
```

```python
compound = input('Enter the compound: ')
if compound == 'H20':
	print('Water')
elif compound == 'NH3':
	print('Ammonia')
elif compound == 'CH4':
	print('Methane')
else:
	print('Unknown compound')


```


#### Nested if statements
```python
value = input('Enter the pH level: ')
if len(value) > 0:
	ph = float(value) 
	if ph < 7.0:
		print(ph, " is acidic.")
	elif ph > 7.0:
		print(ph, " is basic.")
	else:
		print(ph, " is neutral.")

else:
	print('No pH value was given!')

```


```python
if age < 45:
	if bmi < 22.0:
		risk = 'low'
	else:
		risk = 'medium'
else:
	if bmi < 22.0:
		risk = 'medium'
	else:
		risk = 'high'

```

```python
young = age < 45
slim = bmi < 22.0
if young:
	if slim:
		risk = 'low'
	else:
		risk = 'medium'
else:
	if slim:
		risk = 'medium'
	else:
		risk = 'high'
```

```python
young = age < 45
slim = bmi < 22.0
if young and slim:
	risk = 'low'
elif young and not slim :
	risk = 'medium'
elif not young and slim:
	risk = 'medium'
elif not you and not slim:
	risk = 'high'
```

- What is wrong with the following code?
```python
ph = 2
if ph < 7.0:
	print(ph, ' is acidic')
elif ph < 3.0:
	print(ph, ' is VERY acidic! Be careful.')
```

```python
# Implement the min() function for three inputs

number1 = int(input('Enter first integer: '))
number2 = int(input('Enter second integer: '))
number3 = int(input('Enter third integer: '))

minimum = number1  

if number2 < minimum:
    minimum = number2

if number3 < minimum:
    minimum = number3

print('Minimum value is', minimum)
```


https://www.analyzemath.com/Equations/solve-quadratic-equations-using-discriminants.html

## Data Structures (lists, tuples) - python "arrays"
- So far we have covered the following data types: `int`, `float`, and `bool`. Now we will
cover `list`, and `tuple` 
- Data types in Python can be classified as `mutable`, i.e. changeable, and `immutable`, i.e. not changeable. 
    - Immutable data types are: `int`, `float`, `bool`, and `tuple`
    - Mutable data types are: `list`, `dict`, and `set`

Use visualization of variables and memory to find what happens on "changing" variable with immutable data type https://pythontutor.com/visualize.html (config: hide exited frames, rander all objects on the heap and use text labels for pointers)
```python
x=1
id(x)
x=x+2
id(x)
```

In python variables are passed to a function can be though as pass-by-reference. 
That is mutable data types can be changed within function. 
The immutable data can not be changed by definition, 
so sometimes their passage to function can be considered effectively "pass-by-value".



### List
- `list` is a container for storing a sequence of values. The values can be of different type. When the values are all `int`, `float`, or `bool`, you can use special functions. 

#### List Index -- starts at 0
```python
whales = [5, 4, 7, 3, 2, 3, 2, 6, 4, 2, 1, 7, 1, 3]
```

#### Creating a list
```python
grades = ['A', 'B', 'C', 'D', 'F']
```

#### Accessing a list
```python
grades[0]
``` 

#### Slicing a list
```python
grades[2:4]
grades[1::2]
grades[-1]
grades[::-1]
```

#### Reassigning a list
```python
grades = ['A', 'B', 'C', 'D', 'F']
grades[0] = 'a'
grades[1:2] = 'a'
grades[2:] = ['d', 'f']
```

#### Deleting from a list
```python
grades = ['A', 'B', 'C', 'D', 'F']
del grades[0]
del grades[1:3]
del grades
```

#### Concatenate lists
```python
grades1 = ['A', 'B', 'C']
grades2 = ['D', 'F']
grades = grades1 + grades2
```

#### Multiplication
```python
grades = ['A', 'B', 'C', 'D', 'F']
grades *= 3

```

#### Can store different data types
- But you will lose some processing functionality
```python
my_list = ['A', 1, 'Spam', True]
my_list2 = [['John', [55, 65, 86]], ['Jane', [70, 80, 80]]
```

#### Built-in List methods
- `len()` calculate length of list
- `max()` calculate max of list
- `min()` calculate min of list
- `sum()` calculate sum of list
- `sorted()` return a sorted list
- `list()` cast to type list -- convert tuple to list or a generator to list
- `any()` return `True` if the truthiness of any value is `True` in the list
- `all()` return `True` if the truthiness of all the values is `True` in the list

```python
numbers = [3, 4, 8, 9, 5, 6, 7, 0, 1, 2, 10, 11, 12]
len(numbers)
max(numbers)
min(numbers)
sum(numbers)
sorted(numbers)
list(numbers)
any(numbers)
all(numbers)
```
```python
booleans = [True, False, True]
any(booleans)
all(booleans)
```

```python
booleans = [True, True, True]
any(booleans)
all(booleans)
```

#### List methods (functions)
- `append()` - add an element to end of list
- `insert()` - insert an element to the list at the specified location
- `remove()` - remove the element 
- `pop()` - remove the last element in the list; also returns the value; you can save this to another variable
- `clear()` - empty the list
- `index()` - return position of first matching element
- `count()` - count the number of elements
- `sort()` - sort the list in place 
- `reverse()` - reverse the list in place


```python
grades = ['A', 'B', 'C']
grades.append('D')
grades.insert(4, 'F')
grades.remove(2)
grades.pop()
grades.index('C')
grades.count('C') # len(grades)
grades.sort()
grades.reverse()
```

#### List unpacking 
```python
a, b = [3,4]
```

### Tuples
- Tuple are just like lists except that they are immutable. Once you have created a tuple, you cannot modify it.
  - But you still can modify mutable item inside tuple
- Why use them?
- faster than lists
- make code safer -- because you cannot change it
- valid keys in a dictionary

```python
a = ([1], 12)
# a is ([2], 12)

a[0][0]=2
# a is ([2], [12])

a[1]=2 # No-no, you can not change immutable item
```
