I recommend checking out the website, as you can try the code live. The chapters order matches the website's.
> [!NOTE] 
> Source & Reference
> This note uses information from [W3Schools Python Tutorial](https://www.w3schools.com/python). Check it out for interactive exercises and further explanations.

---

## 1. How to Output Strings

Strings can be enclosed in either single (`'`) or double (`"`) quotes. You can also use f-strings to embed variables directly.

```python
print("hello world!")
print('also correct')

a = 25
print(f"I am {a} years old")
```

---

## 2. How to Comment

Python supports single-line comments using `#` and multi-line comments using triple-quoted string literals.

```python
# one row commentary

"""
multiple rows commentary
"""
```

---

## 3. How to Output on the Same Line Using `end`

By default, `print()` ends with a newline. Use the `end` parameter to specify a different ending character (like a space).

```python
print("hello world", end=" ")
print("I will print on the same line")
```

---

## 4. How to Print Numbers and Operations

You can print numbers and math expressions directly.

```python
print(5)
print(5 * 4)
```

---

## 5. Outputting a Combination of Strings and Numbers/Variables

Use commas `,` to separate strings and other data types inside `print()`. Python will automatically add spaces between them.

```python
print("I am", 20, "years old")
```

---

## 6. How to Create a Variable

You do not need to declare a variable type when creating it, though you can specify types using casting.

> [!WARNING] 
> Case Sensitivity
> Variable names are case-sensitive: `x` is not the same as `X`.

```python
x = 3           # x is of type int
x = str(3)      # x will be '3'
y = int(3)      # y will be 3
z = float(3)    # z will be 3.0

# Multiple assignment:
x, y, z = "Orange", "Banana", 7
```

---

## 7. How to Get the Type of a Variable

Use the `type()` built-in function to inspect the type of any object:

```python
x = 5
y = "John"

print(type(x))  # <class 'int'>
print(type(y))  # <class 'str'>
```

---

## 8. Unpack a Collection

If you have a collection of values (like a list or tuple), you can unpack them directly into variables:

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits

print(x)
print(y)
print(z)
```

---

## 9. How to Output Multiple Variables

You can output multiple variables separated by commas or concatenated with `+`:

```python
print(x, y, z)
print(x + y + z)
```

> [!NOTE] 
> Behavior of `+`
> - For numbers, `+` acts as mathematical addition.
> - For strings, `+` concatenates without adding spaces.
> - You cannot combine strings and numbers using `+`.

---

## 10. How to Make a Global Variable (`global` keyword)

To create or modify a variable at the global scope from inside a function, use the `global` keyword:

```python
def myfunc():
    global x
    x = "fantastic"

myfunc()

print("Python is " + x)
```

---

## 11. Data Types

| Type        | Name           | Description                                               | Example                          |
| :---------- | :------------- | :-------------------------------------------------------- | :------------------------------- |
| `str`       | Text           | Textual data                                              | `"Hello"`                        |
| `int`       | Integer        | Whole numbers                                             | `20`, `-5`                       |
| `float`     | Floating Point | Decimal numbers or scientific notation ($15 \times 10^3$) | `15e3`, `3.14`                   |
| `complex`   | Complex        | Numbers belonging to $\mathbb{C}$                         | `1j`                             |
| `range`     | Sequence       | Sequence of numbers (e.g. `range(3, 5, 1)` $\to$ `3, 4`)  | `range(4)` $\to$ `0, 1, 2, 3`    |
| `list`      | List           | Modifiable, ordered, allows duplicates                    | `["apple", "banana", "cherry"]`  |
| `tuple`     | Tuple          | Unmodifiable, ordered, allows duplicates                  | `("apple", "banana", "cherry")`  |
| `set`       | Set            | Modifiable, unordered, unindexed, no duplicates           | `{"apple", "banana", "cherry"}`  |
| `dict`      | Dictionary     | Modifiable collection of key-value pairs                  | `{"name": "John", "age": 36}`    |
| `frozenset` | Frozen Set     | Immutable version of a set                                | `frozenset({"apple", "banana"})` |
| `bool`      | Boolean        | Truth values                                              | `True`, `False`                  |

* **Advanced/Binary types:** `bytes`, `bytearray`, `memoryview`, `NoneType`.

---

## 12. Type Conversion

### Numeric Conversion
```python
x = 5
x = float(x)    # Converts int to float (5.0)

z = float("3")  # z becomes 3.0 even though source is a string
w = int(4.567)  # w becomes 4 (truncates decimals)
```

> [!WARNING]
> You cannot convert complex numbers into another number type.

### String Conversion
```python
x = str(3)      # Converts integer 3 to string '3'
```

---

## 13. Random Number Generator

Python includes a built-in `random` module to work with random numbers:

```python
import random

# Generate a random integer from 1 to 9 (10 is excluded)
print(random.randrange(1, 10))
```

---

## 14. Quotes Inside Quotes

You can use quotes inside a string as long as they do not match the surrounding quotes:

```python
print("It's alright")
print("He is called 'Johnny Joestar'")
print('He is called "Johnny Joestar"')
```

---

## 15. Strings

### Multiline Strings
Assign multiline strings using triple single or double quotes:

```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
```

### Strings as Arrays (Vectors)
Strings are arrays of bytes representing unicode characters. Indexing starts at `0`:

```python
a = "Hello, World!"
print(a[1])  # 'e'
```

### Looping Through a String
```python
for x in "banana":
    print(x)
```

### String Length
```python
a = "Hello, World!"
print(len(a))
```

### Check String (`in` / `not in`)
Returns a boolean (`True` or `False`):

```python
txt = "The best things in life are free!"
print("free" in txt)

if "expensive" not in txt:
    print("No, 'expensive' is NOT present.")
```

### Slicing Strings
Specify the start index and end index, separated by a colon (end index is excluded):

```python
b = "Hello, World!"

# Slice specific range
print(b[2:5])   # "llo"

# Slice from the start
print(b[:5])    # "Hello"

# Slice to the end
print(b[2:])    # "llo, World!"

# Negative indexing
print(b[-5:-2]) # "orl"
```

```text
 H   e   l   l   o   ,       W   o   r   l   d   !
                                -5  -4  -3  -2  -1
```

### String Modification Methods
```python
a = " Hello, World! "

# Case changes
print(a.upper()) #HELLO, WORLD!
print(a.lower())

# Remove whitespace before and after
print(a.strip())  # "Hello, World!"

# Replace string (case-sensitive)
print(a.replace("H", "J")) #Jello, World!

# Split string into substrings by separator
b = a.split(",")  # Returns [' Hello', ' World! '] the "," is the point of splitting and is not included anymore
```

### Concatenation
```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)
```

### Formatted Strings (f-strings)
Format strings combine numbers and strings directly, format decimal points, and evaluate inline expressions:

```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)

# Specify number of decimals:
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)  # "The price is 59.00 dollars"

# Inline math operations:
txt = f"The price is {20 * 59} dollars"
print(txt)  # "The price is 1180 dollars"
```

> [!TIP] 
> Further Resources
> - [W3Schools String Escape Characters Reference](https://www.w3schools.com/python/python_strings_escape.asp)
> - [W3Schools String Methods Reference](https://www.w3schools.com/python/python_strings_methods.asp) - will check certain proprieties for strings

---

## 16. Booleans

Booleans represent one of two values: `True` or `False`.

* Almost any value is evaluated to `True` if it has some sort of content.
* Any string is `True`, except empty strings (`""`).
* Any number is `True`, except `0`.
* Any list, tuple, set, and dictionary are `True`, except empty ones (`[]`, `()`, `{}`, `set()`).

Python also has built-in functions that return a boolean value, such as `isinstance()`, which determines if an object belongs to a specified data type:

```python
x = 200
print(isinstance(x, int))  # True
print(isinstance(x, str))  # False
```

---

## 17. Operators

### Arithmetic Operators

| Operator | Name | Example |
| :--- | :--- | :--- |
| `+` | Addition | `x + y` |
| `-` | Subtraction | `x - y` |
| `*` | Multiplication | `x * y` |
| `/` | Division | `x / y` |
| `%` | Modulus | `x % y` |
| `**` | Exponentiation | `x ** y` |
| `//` | Floor division | `x // y` |

---

### Assignment Operators

| Operator | Example | Same As |
| :--- | :--- | :--- |
| `=` | `x = 5` | `x = 5` |
| `+=` | `x += 3` | `x = x + 3` |
| `-=` | `x -= 3` | `x = x - 3` |
| `*=` | `x *= 3` | `x = x * 3` |
| `/=` | `x /= 3` | `x = x / 3` |
| `%=` | `x %= 3` | `x = x % 3` |
| `//=` | `x //= 3` | `x = x // 3` |
| `**=` | `x **= 3` | `x = x ** 3` |
| `&=` | `x &= 3` | `x = x & 3` |
| `\|=` | `x \|= 3` | `x = x \| 3` |
| `^=` | `x ^= 3` | `x = x ^ 3` |
| `>>=` | `x >>= 3` | `x = x >> 3` |
| `<<=` | `x <<= 3` | `x = x << 3` |
| `:=` | `print(x := 3)` | `x = 3`<br>`print(x)` 
The walrus operator (introduced python 3.8) allows to give value in the same statement
```python
numbers = [1, 2, 3, 4, 5]  
  
if (count := len(numbers)) > 3:  
    print(f"List has {count} elements")
```

---
### Ternary Operator
The ternary operator allows you to assign one value if a condition is true, and another if it is false:
```python
num = 6  
  
x = "Fri" if num == 5 else "Sat" if num == 6 else "Sun" if num == 7 else "weekday"  
  
print(x)
```

---
### Comparison Operators
| Operator | Name                     | Example |
| -------- | ------------------------ | ------- |
| ==       | Equal                    | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y  |

Python also allows you to chain operators
```python
x = 5  
  
print(1 < x < 10) #true 
  
print(1 < x and x < 10) #true
```

---
### Logical operators
| Operator | Description                                             | Example               |
| -------- | ------------------------------------------------------- | --------------------- |
| and      | Returns True if both statements are true                | x < 5 and  x < 10     |
| or       | Returns True if one of the statements is true           | x < 5 or x < 4        |
| not      | Reverse the result, returns False if the result is true | not(x < 5 and x < 10) |

---
### Identity operators
| Operator | Description                                            | Example    |
| -------- | ------------------------------------------------------ | ---------- |
| is       | Returns True if both variables are the same object     | x is y     |
| is not   | Returns True if both variables are not the same object | x is not y |
```python
#EXAMPLE
x = ["apple", "banana"]  
y = ["apple", "banana"]  
z = x  
  
print(x is z)  #TRUE
print(x is y)  #FALSE
print(x == y)  #TRUE

# is checks identity, == checks value
```
---
### Membership operators
| Operator | Description                                                                      | Example    |
| -------- | -------------------------------------------------------------------------------- | ---------- |
| in       | Returns True if a sequence with the specified value is present in the object     | x in y     |
| not in   | Returns True if a sequence with the specified value is not present in the object | x not in y |
```python
fruits = ["apple", "banana", "cherry"]  
  
print("banana" in fruits) #true
```
---
### Bitwise Operators
| Operator | Name                 | Description                                                                                             | Example |
| -------- | -------------------- | ------------------------------------------------------------------------------------------------------- | ------- |
| &        | AND                  | Sets each bit to 1 if both bits are 1                                                                   | x & y   |
| \|       | OR                   | Sets each bit to 1 if one of two bits is 1                                                              | x \| y  |
| ^        | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         | x ^ y   |
| ~        | NOT                  | Inverts all the bits                                                                                    | ~x      |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        | x << 2  |
| >>       | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2  |
#### Example

The & operator compares each bit and set it to 1 if both are 1, otherwise it is set to 0:
```python
print(6 & 3)
```

The binary representation of 6 is 0110  
The binary representation of 3 is 0011

Then the & operator compares the bits and returns 0010, which is 2 in decimal.

---
### Operator Precedence
| Operator                                                         | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| `()`                                                             | Parentheses                                           |
| `**`                                                             | Exponentiation                                        |
| `+x`  `-x`  `~x`                                                 | Unary plus, unary minus, and bitwise NOT              |
| `*`  `/`  `//`  `%`                                              | Multiplication, division, floor division, and modulus |
| `+`  `-`                                                         | Addition and subtraction                              |
| `<<`  `>>`                                                       | Bitwise left and right shifts                         |
| `&`                                                              | Bitwise AND                                           |
| `^`                                                              | Bitwise XOR                                           |
| `\|`                                                             | Bitwise OR                                            |
| `==`  `!=`  `>`  `>=`  `<`  `<=`  `is`  `is not`  `in`  `not in` | Comparisons, identity, and membership operators       |
| `not`                                                            | Logical NOT                                           |
| `and`                                                            | AND                                                   |
| `or`                                                             | OR                                                    |
Also keep in mind that when there are same precedence level, it will be evaluated from left to right.

---
## 18. Lists
Lists are used to store multiple items in a single variable. Lists are ORDERED, CHANGABLE and ALLOW DUPLICATES (the most permissive). Lists are indexed from 0.
```python
#visualize indexing
thislist = ["abc", 34, True, 40, "male"]
#            0,    1,   2,   3,   4
#            -5,   -4,  -3,  -2,  -1
```
### Creating a list
```python
thislist = ["abc", 34, True, 40, "male"]
# alternative way of creating a list 
otherlist = list(("apple", "banana", "cherry")) # note the double round-brackets
```
### Printing a list
```python
print(thislist) # prints the whole list with paretheses and separated by commas
print(len(thislist)) # 5
print(type(thislist)) # <class 'list'>
print(thislist[1]) # 34
print(thislist[-1]) # "male"
print(thislist[2:4]) # True, 40 returns the 3rd and 4th element: the element index from 2 (included) to 4 (not included)
print(thislist[:3]) # prints everything from beginning to the element in index 3 (not included)
print(thislist[2:]) # prints everything from the element indexed with 2 (included)
print(thislist[-4:-1]) # prints from 34 (included)
if "abc" in thislist:  
  print("Yes, 'abc' is in the list")
```

### Editing a list
```python

thislist[1] = "def" #changes the element indexed as 1
thislist[1:3] = ["def", "jam"] #changes elements [1,3)
thislist[1:2] = ["blackcurrant", "watermelon"] #changes element 1 and adds the rest of them, so even if it changes 1 element, it adds the extra elements after the changed element, so the lenght increases
thislist.insert(2, "stuff") #inserts as the 3rd element "stuff" (index 2)
```
### Adding to a list
```python
thislist.append("orange") # appends elements
thislist.extend(otherlist) # appends otherlist to thislist
thislist.extend(#whatever stucture) #also works for appending other stuctures types (tuple, set, dict)
```
### Removing from a list
```python
thislist.remove("male") #removes element
thislist.pop(1) #removes 2nd element (indexed 1)
thislist.pop() #removes the last element
del thislist[0] # deletes the first element
del thislist # deletes the entire list ; print(thislist) afterwards will cause an error
thislist.clear() # clears the list; the list remains, but it's empty
```
### Looping through a list
```python

thislist = ["apple", "banana", "cherry"]  
for x in thislist:  # loops until all elements are printed
  print(x)
  
for i in range(len(thislist)):  # loops through index e
  print(thislist[i])
  
i = 0  
while i < len(thislist):  
  print(thislist[i])  
  i = i + 1
  
[print(x) for x in thislist]
```
### List comprehesion
```python
SYNTAX: newlist = [expression for item in iterable if condition == True]
#the contition will return the elements for which the condition is true, but this can be omitted

#example 1 : how it looks without list comprehesion
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]  
newlist = []  
  
for x in fruits:  
  if "a" in x:  
    newlist.append(x)  
  
print(newlist)

#example 2: list comprehesion applied to example 1
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]  
  
newlist = [x for x in fruits if "a" in x]  
  
print(newlist)

#example 3: set new values to uppercase with no condition
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x.upper() for x in fruits] #['APPLE', 'BANANA', 'CHERRY', 'KIWI', 'MANGO']

newlist = [x if x != "banana" else "orange" for x in fruits] #['apple', 'orange', 'cherry', 'kiwi', 'mango']
```
### List sorting
```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]  
thislist.sort() #alphanumerical ascending sorting
thislist.sort(reverse = True) #alphanumerical descending sorting

thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower) #case unsensitive sorting
thislist.sort(key = str.lower, reverse = True) # descending case unsensitive sorting
thislist.reverse() # ['cherry', 'Kiwi', 'Orange', 'banana'] , reverse of the current order
```
### Copy lists
Doing list2 = list1 will not copy the list, but will instead be a reference to the original list.
```python
thislist = ["apple", "banana", "cherry"]  
mylist = thislist.copy() # method 1
mylist = list(thislist) # method 2
mylist = thislist[:] # method 3
mylist = thislist[:2] #copy only the first two elements
mylist = thislist[1:2] #copy only the second element
```
### Join lists
```python
list1 = ["a", "b", "c"]  
list2 = [1, 2, 3]  
  
list3 = list1 + list2 #method 1 : make a new list
for x in list2:  #method 2 : append to list1 list2
  list1.append(x)
list1.extend(list2) #method 3 : extend list1
```
### List methods
|Method|Description|
|---|---|
|[append()](https://www.w3schools.com/python/ref_list_append.asp)|Adds an element at the end of the list|
|[clear()](https://www.w3schools.com/python/ref_list_clear.asp)|Removes all the elements from the list|
|[copy()](https://www.w3schools.com/python/ref_list_copy.asp)|Returns a copy of the list|
|[count()](https://www.w3schools.com/python/ref_list_count.asp)|Returns the number of elements with the specified value|
|[extend()](https://www.w3schools.com/python/ref_list_extend.asp)|Add the elements of a list (or any iterable), to the end of the current list|
|[index()](https://www.w3schools.com/python/ref_list_index.asp)|Returns the index of the first element with the specified value|
|[insert()](https://www.w3schools.com/python/ref_list_insert.asp)|Adds an element at the specified position|
|[pop()](https://www.w3schools.com/python/ref_list_pop.asp)|Removes the element at the specified position|
|[remove()](https://www.w3schools.com/python/ref_list_remove.asp)|Removes the item with the specified value|
|[reverse()](https://www.w3schools.com/python/ref_list_reverse.asp)|Reverses the order of the list|
|[sort()](https://www.w3schools.com/python/ref_list_sort.asp)|Sorts the list|
## 19. Tuples
Tuples are used to store multiple items in a single variable. Tuples are ORDERED, IMMUTABLE (unchangeable) and ALLOWS DUPLICATES. Tuples are indexed from 0 same as lists (same negative indexing as well).
### Creating a tuple
```python
thistuple = ("apple", "banana", "cherry", "apple", "cherry") #method 1
thistuple = "apple", "banana", "cherry" #method 2
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets, method 3

#CREATING A TUPLE WITH ONE ELEMENT
thistuple = ("apple",)  
print(type(thistuple))  #TUPLE
  
#NOT a tuple  
thistuple = ("apple")  
print(type(thistuple)) #STR

thistuple = () #void tuple

tuple1 = ("abc", 34, True, 40, "male") #tuple can contain different data types
```
### Access tuples
```python
thistuple = ("apple", "banana", "cherry")  
print(thistuple[1]) # banana
print(thistuple[-1]) #cherry

thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")  
print(thistuple[2:5]) # ('cherry', 'orange', 'kiwi')
print(thistuple[:4]) # ('apple', 'banana', 'cherry', 'orange')
print(thistuple[2:]) # ('cherry', 'orange', 'kiwi', 'melon', 'mango')

thistuple = ("apple", "banana", "cherry")  
if "apple" in thistuple:  
  print("Yes, 'apple' is in the fruits tuple")
```

### Update tuples
We already established that we can't modify tuples, but there is a workaround. We can easily convert a tuple to a list and edit it afterwards. In the end, we can convert it back to a tuple. This can be used to add or remove items.

```python
thistuple = ("apple", "banana", "cherry")  
y = list(thistuple)  
y.remove("apple")  
thistuple = tuple(y) #("banana", "cherry")

#you can also delete a tuple
del thistuple
print(thistuple) # error

#also for adding items, you can add a tuple to another tuple
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y # ('apple', 'banana', 'cherry', 'orange')
```
###