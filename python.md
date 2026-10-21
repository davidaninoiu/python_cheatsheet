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
### Unpack tuples
Creating a tuple means packing it, so the reverse is making more variables or lists from an existing one. Unpacking a tuple must always match the number of elements, or else it. will give an error
```python
#variables
fruits = ("apple", "banana", "cherry")  
(green, yellow, red) = fruits

#variables and list, red will take the remaining elements (notice the *)
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")  
(green, yellow, *red) = fruits

#variables and a list in the middle
fruits = ("apple", "mango", "papaya", "pineapple", "cherry")  
(green, *tropic, red) = fruits

#error
fruits = ("apple", "banana", "cherry")  
(green, yellow) = fruits
```
### Loop tuples
```python
thistuple = ("apple", "banana", "cherry")  #for
for x in thistuple:  
  print(x)

thistuple = ("apple", "banana", "cherry")  #for, index numbers
for i in range(len(thistuple)):  
  print(thistuple[i])

thistuple = ("apple", "banana", "cherry")  #while
i = 0  
while i < len(thistuple):  
  print(thistuple[i])  
  i = i + 1
```
### Join tuples
```python
tuple1 = ("a", "b" , "c")  
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2

fruits = ("apple", "banana", "cherry")  
mytuple = fruits * 2
	print(mytuple) #('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')
```
### Tuple methods
|Method|Description|
|---|---|
|[count()](https://www.w3schools.com/python/ref_tuple_count.asp)|Returns the number of times a specified value occurs in a tuple|
|[index()](https://www.w3schools.com/python/ref_tuple_index.asp)|Searches the tuple for a specified value and returns the position of where it was found
## 20. Sets
Sets are used to store multiple items in a single variable. Sets are UNORDERED, UNINDEXED, UNCHANGABLE (can't change the actual value, but can add an remove values), and does NOT ALLOW DUPLICATES.

### Create sets
```python
thisset = {"apple", "banana", "cherry"}
thisset = set(("apple", "banana", "cherry")) # note the double round-brackets
thisset = {"apple", "banana", "cherry", True, 1, 2} #True and 1 are considered the same value. Same goes for False and 0
```
### Access set items
While you can't change items, you can add or remove items. 

> [!warning]
> You cannot access items via index, because there isn't one


```python
thisset = {"apple", "banana", "cherry"}  
  
for x in thisset:  
  print(x) # prints all items
print("banana" in thisset) # True
print("banana" not in thisset) # False
```
### Add items in a set
```python
thisset = {"apple", "banana", "cherry"}  
thisset.add("orange")

thisset = {"apple", "banana", "cherry"}  
tropical = {"pineapple", "mango", "papaya"}  
thisset.update(tropical) # adds elements from tropical to thisset

thisset = {"apple", "banana", "cherry"}  
mylist = ["kiwi", "orange"]  
thisset.update(mylist) #also works for adding elements from other data types
```

### Remove items in a set
```python
thisset = {"apple", "banana", "cherry"}  
thisset.remove("banana") # if the item removed does not exist at first, it will give an error
thisset.discard("cherry") # if the item removed does not exist at first, it will NOT give an error
x = thisset.pop() #removes a random item
thisset.clear() #gives a void set
del thisset #deletes the set altogether, cannot be accessed afterwards
```

### Loop sets
```python
thisset = {"apple", "banana", "cherry"}  #only valid way, since items are indexless. output will be random
  
for x in thisset:  
  print(x)
```
### Join sets
>[!NOTE]
>There are several ways to join two or more sets in Python.
>
>The [union()](https://www.w3schools.com/python/ref_set_union.asp) and [update()](https://www.w3schools.com/python/ref_set_update.asp) methods joins all items from both sets. Also there is `|`.
>
>The [intersection()](https://www.w3schools.com/python/ref_set_intersection.asp) method keeps ONLY the duplicates. Also there is `&`.
> 
>The [difference()](https://www.w3schools.com/python/ref_set_difference.asp) method keeps the items from the first set that are not in the other set(s). Also there is `-`.
>
>The [symmetric_difference()](https://www.w3schools.com/python/ref_set_symmetric_difference.asp) method keeps all items EXCEPT the duplicates. Also there is `^`.
>
>Note that `| , &, -, ^` can only be used between set, while the methods can be used between a set and a different data type. You can also see a pattern with `_update` being added to the method that will edit the initial set instead of creating a new one.


#### Union
```python
set1 = {"a", "b", "c"}  
set2 = {1, 2, 3}  
  
set3 = set1.union(set2)  
print(set3) # {1, 'b', 3, 2, 'c', 'a'}


x = {"a", "b", "c"}  
y = (1, 2, 3)  
  
z = x.union(y)  # added a tuple to a set
print(z)
```
Example of `|`
```python
set1 = {"a", "b", "c"}  
set2 = {1, 2, 3}  
set3 = {"John", "Elena"}  
set4 = {"apple", "bananas", "cherry"}  
  
myset = set1 | set2 | set3 |set4  
print(myset) # {banana, John, apple, 1, 3, 'a', cherry, Elena, 'b', 'c', 2}
```

#### Update
```python 
set1 = {"a", "b" , "c"}  
set2 = {1, 2, 3}  
  
set1.update(set2)  
print(set1)
```
>[!warning]
>Note that both union and update remove any duplicates.

#### Intersection
```python
set1 = {"apple", "banana", "cherry"}  
set2 = {"google", "microsoft", "apple"}  
  
set3 = set1.intersection(set2) # {'apple'}
set3 = set1 & set2 # method 2
set1.intersection_update(set2) # will only keep duplicates, but instead of returning a new set, it will update your set
```

#### Difference
```python
set1 = {"apple", "banana", "cherry"}  
set2 = {"google", "microsoft", "apple"}  
  
set3 = set1.difference(set2) #method 1 ; {'banana', 'cherry'}
set3 = set1 - set2 #method 2, using operator
set1.difference_update(set2) #method 3, formatting the initial set
```

#### Symmetric difference
```python
set1 = {"apple", "banana", "cherry"}  
set2 = {"google", "microsoft", "apple"}  
  
set3 = set1.symmetric_difference(set2) # {'google', 'banana', 'microsoft', 'cherry'}
set3 = set1 ^ set2
set1.symmetric_difference_update(set2)
```

### Frozenset
`frozenset` is an immutable version of a set.
Like sets, it contains unique, unordered, unchangeable elements.
Unlike sets, elements cannot be added or removed from a frozenset.

Being immutable means you cannot add or remove elements. However, frozensets support all non-mutating operations of sets.
```python
x = frozenset({"apple", "banana", "cherry"})  
print(x)  
print(type(x)) #<class 'frozenset'>
```

### Set methods
| Method                                                                                                    | Shortcut                                                                       | Description                                                                    |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| [add()](https://www.w3schools.com/python/ref_set_add.asp)                                                 |                                                                                | Adds an element to the set                                                     |
| [clear()](https://www.w3schools.com/python/ref_set_clear.asp)                                             |                                                                                | Removes all the elements from the set                                          |
| [copy()](https://www.w3schools.com/python/ref_set_copy.asp)                                               |                                                                                | Returns a copy of the set                                                      |
| [difference()](https://www.w3schools.com/python/ref_set_difference.asp)                                   | [-](https://www.w3schools.com/python/ref_set_difference.asp)                   | Returns a set containing the difference between two or more sets               |
| [difference_update()](https://www.w3schools.com/python/ref_set_difference_update.asp)                     | [-=](https://www.w3schools.com/python/ref_set_difference_update.asp)           | Removes the items in this set that are also included in another, specified set |
| [discard()](https://www.w3schools.com/python/ref_set_discard.asp)                                         |                                                                                | Remove the specified item                                                      |
| [intersection()](https://www.w3schools.com/python/ref_set_intersection.asp)                               | [&](https://www.w3schools.com/python/ref_set_intersection.asp)                 | Returns a set, that is the intersection of two other sets                      |
| [intersection_update()](https://www.w3schools.com/python/ref_set_intersection_update.asp)                 | [&=](https://www.w3schools.com/python/ref_set_intersection_update.asp)         | Removes the items in this set that are not present in other, specified set(s)  |
| [isdisjoint()](https://www.w3schools.com/python/ref_set_isdisjoint.asp)                                   |                                                                                | Returns True if NO items of this set is present in another set                 |
| [issubset()](https://www.w3schools.com/python/ref_set_issubset.asp)                                       | [<=](https://www.w3schools.com/python/ref_set_issubset.asp)                    | Returns True if all items of this set is present in another set                |
|                                                                                                           | [<](https://www.w3schools.com/python/ref_set_lessthan.asp)                     | Returns True if all items of this set is present in another, _larger_ set      |
| [issuperset()](https://www.w3schools.com/python/ref_set_issuperset.asp)                                   | [>=](https://www.w3schools.com/python/ref_set_issuperset.asp)                  | Returns True if all items of another set is present in this set                |
|                                                                                                           | [>](https://www.w3schools.com/python/ref_set_greaterthan.asp)                  | Returns True if all items of another, _smaller_ set is present in this set     |
| [pop()](https://www.w3schools.com/python/ref_set_pop.asp)                                                 |                                                                                | Removes an element from the set                                                |
| [remove()](https://www.w3schools.com/python/ref_set_remove.asp)                                           |                                                                                | Removes the specified element                                                  |
| [symmetric_difference()](https://www.w3schools.com/python/ref_set_symmetric_difference.asp)               | [^](https://www.w3schools.com/python/ref_set_symmetric_difference.asp)         | Returns a set with the symmetric differences of two sets                       |
| [symmetric_difference_update()](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | [^=](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | Inserts the symmetric differences from this set and another                    |
| [union()](https://www.w3schools.com/python/ref_set_union.asp)                                             | [\|](https://www.w3schools.com/python/ref_set_union.asp)                       | Return a set containing the union of sets                                      |
| [update()](https://www.w3schools.com/python/ref_set_update.asp)                                           | [\|=](https://www.w3schools.com/python/ref_set_update.asp)                     | Update the set with the union of this set and others                           |

## 21. Dictionaries
> [!WARNING]
>`*` As of Python version 3.7, dictionaries are _ordered_. In Python 3.6 and earlier, dictionaries are _unordered_.

Dictionaries are used to store data values in key:value pairs.
A dictionary is a collection which is ORDERED*, CHANGEABLE and do NOT ALLOW DUPLICATES.

### Create a dictionary
```python 
thisdict = {  #like all the other data types for storing items, you can have multiple data types inside
  "brand": "Ford",  
  "electric": False,  
  "year": 1964,  
  "colors": ["red", "white", "blue"]  
}
print(thisdict) #{'brand': 'Ford', 'electric': False, 'year': 1964, 'colors': ['red', 'white', 'blue']}
print(thisdict["brand"]) # Ford

thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964,  
  "year": 2020  #since duplicates are not allowed, this will overwrite the existing "year"
}  
print(thisdict) #{'brand': 'Ford', 'model': 'Mustang', 'year': 2020}
```

### Access items in a dictionary
```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
x = thisdict["model"] # method 1 , Mustang
x = thisdict.get("model") # method 2
x = thisdict.keys() # dict_keys(['brand', 'model', 'year'])
x = thisdict.values() # dict_values(['Ford', 'Mustang', 1964])
```
The list of the keys is a _view_ of the dictionary, meaning that any changes done to the dictionary will be reflected in the keys list.
```python
car = {  
"brand": "Ford",  
"model": "Mustang",  
"year": 1964  
}  
  
if "model" in thisdict:  
  print("Yes, 'model' is one of the keys in the thisdict dictionary") #check if a certain key is inside the dictionary
x = car.keys()  
print(x) # dict_keys(['brand', 'model', 'year'])
car["color"] = "white"  
print(x) # dict_keys(['brand', 'model', 'year', 'color'])
```
This works similarly for the values method. Notice how x gets updated, since it's not a regular variable.
```python
car = {  
"brand": "Ford",  
"model": "Mustang",  
"year": 1964  
}  
  
x = car.values()  
  
print(x) #dict_values(['Ford', 'Mustang', 1964])
  
car["year"] = 2020  
  
print(x) #dict_values(['Ford', 'Mustang', 2020])

car["color"] = "red"  
  
print(x) #dict_values(['Ford', 'Mustang', 2020, 'red'])
```
There is also a way to get all items in tuples, list that gets updated as well.
```python
car = {  
"brand": "Ford",  
"model": "Mustang",  
"year": 1964  
}  
  
x = car.items()  
  
print(x) #dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)]) 
  
car["year"] = 2020  
  
print(x) #dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 2020)])
```

### Change values
```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
thisdict["year"] = 2018 #method 1
thisdict.update({"year": 2020}) #method 2
```

### Add items
```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
thisdict["color"] = "red" #method 1
thisdict.update({"color": "red"}) #method 2
```

### Remove items
```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
thisdict.pop("model") #eliminates model
thisdict.pop() # eliminates the last element in dictionary as of python 3.7. before 3.7, eliminates random item
del thisdict["model"] #eliminates model
del thisdict #eliminates dictionary entirely
thisdict.clear() #clears dictionary
```

### Loop dictionaries
```python
for x in thisdict:  # Print all key names in the dictionary, one by one
  print(x)
  
for x in thisdict:  #Print all VALUES in the dictionary, one by one
  print(thisdict[x])
  
for x in thisdict.values():  # Print all values
  print(x)
  
for x in thisdict.keys():  # Print all keys
  print(x)
  
for x, y in thisdict.items():  #Print all keys and values like shown under
  print(x, y) 
"""brand Ford  
model Mustang  
year 1964"""
```

### Copy dictionaries
Like other storing data types, you can't copy dictionaries like this : dict1=dict. This method will only attribute a reference of dict to dict1. However, you can copy it by typing it's data type: dict1 = dict(dict) ; or by using .copy()
```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
mydict = thisdict.copy() #method 1
mydict = dict(thisdict) #method 2
```

### Nested dictionaries
Having directories within directories is possible 
```python
myfamily = {  #create nested directories method 1
  "child1" : {  
    "name" : "Emil",  
    "year" : 2004  
  },  
  "child2" : {  
    "name" : "Tobias",  
    "year" : 2007  
  },  
  "child3" : {  
    "name" : "Linus",  
    "year" : 2011  
  }  
}

#create nested directories method 2
child1 = {  
  "name" : "Emil",  
  "year" : 2004  
}  
child2 = {  
  "name" : "Tobias",  
  "year" : 2007  
}  
child3 = {  
  "name" : "Linus",  
  "year" : 2011  
}  
  
myfamily = {  
  "child1" : child1,  
  "child2" : child2,  
  "child3" : child3  
}

print(myfamily["child2"]["name"]) #accessing data from such a dictionary

for x, obj in myfamily.items():  #looping throgh such a dictionary
  print(x)  
  
  for y in obj:  
    print(y + ':', obj[y])
```

### Dictionary methods
| Method                                                                         | Description                                                                                                 |
| ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------- |
| [clear()](https://www.w3schools.com/python/ref_dictionary_clear.asp)           | Removes all the elements from the dictionary                                                                |
| [copy()](https://www.w3schools.com/python/ref_dictionary_copy.asp)             | Returns a copy of the dictionary                                                                            |
| [fromkeys()](https://www.w3schools.com/python/ref_dictionary_fromkeys.asp)     | Returns a dictionary with the specified keys and value                                                      |
| [get()](https://www.w3schools.com/python/ref_dictionary_get.asp)               | Returns the value of the specified key                                                                      |
| [items()](https://www.w3schools.com/python/ref_dictionary_items.asp)           | Returns a list containing a tuple for each key value pair                                                   |
| [keys()](https://www.w3schools.com/python/ref_dictionary_keys.asp)             | Returns a list containing the dictionary's keys                                                             |
| [pop()](https://www.w3schools.com/python/ref_dictionary_pop.asp)               | Removes the element with the specified key                                                                  |
| [popitem()](https://www.w3schools.com/python/ref_dictionary_popitem.asp)       | Removes the last inserted key-value pair                                                                    |
| [setdefault()](https://www.w3schools.com/python/ref_dictionary_setdefault.asp) | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| [update()](https://www.w3schools.com/python/ref_dictionary_update.asp)         | Updates the dictionary with the specified key-value pairs                                                   |
| [values()](https://www.w3schools.com/python/ref_dictionary_values.asp)         | Returns a list of all the values in the dictionary                                                          |

## 22. IF ... ELSE
The `if` statement needs a condition that evaluates to true or false to know whether to execute the next lines or to ignore them. See the sythax below, and notice the indentation (spaces left on the line after the if).
```python
a = 33  
b = 200  
if b > a:  #true
  print("b is greater than a")
```
There is also `elif` that is just else if, an if that evaluates if the first one is false
```python
a = 33  
b = 33  
if b > a:  
  print("b is greater than a")  
elif a == b:  
  print("a and b are equal")
```
Also there is `else`. I will not explain it, since it's pretty obvious, but feel free to check out the [website](https://www.w3schools.com/python/python_conditions.asp) for extra information.
```python
a = 200  
b = 33  
if b > a:  
  print("b is greater than a")  
elif a == b:  
  print("a and b are equal")  
else:  
  print("a is greater than b")
```
You can write if...else on a single line.
```python
a = 2  
b = 330  
bigger = a if a > b else b
print("Bigger is", bigger)
print("A") if a > b else print("B")

a = 330  
b = 330  
print("A") if a > b else print("=") if a == b else print("B")
```
You can also use logical operators.
```python
a = 200  
b = 33  
c = 500  
if a > b or a > c:  
  print("At least one of the conditions is True")
```
You can also have nested ifs.
```python
x = 41  
  
if x > 10:  
  print("Above ten,")  
  if x > 20:  
    print("and also above 20!")  
  else:  
    print("but not above 20.")
```
If you wish to implement and if statement, but you are not ready to write it, you can use `pass` to avoid getting an error for missing instructions.
```python
a = 33  
b = 200  
  
if b > a:  
  pass
```

## 23. Match
Instruction similar with switch from C++, it has cases. There is a default case with the `_` character, which is not mandatory, and you can also combine values. You can also add extra conditions with an `if` after the case.
```python
day = 4  
match day:  
  case 1:  
    print("Monday")  
  case 2:  
    print("Tuesday")  
  case 3:  
    print("Wednesday")  
  case 4:  
    print("Thursday")  
  case 5:  
    print("Friday")  
  case 6:  
    print("Saturday")  
  case 7:  
    print("Sunday")
    
    
day = 4  
match day:  
  case 6:  
    print("Today is Saturday")  
  case 7:  
    print("Today is Sunday")  
  case _:  #default case
    print("Looking forward to the Weekend")
    
    
day = 4  
match day:  
  case 1 | 2 | 3 | 4 | 5:  #combined values
    print("Today is a weekday")  
  case 6 | 7:  
    print("I love weekends!")
    
month = 5  
day = 4  
match day:  
  case 1 | 2 | 3 | 4 | 5 if month == 4:  #add extra condition
    print("A weekday in April")  
  case 1 | 2 | 3 | 4 | 5 if month == 5:  
    print("A weekday in May")  
  case _:  
    print("No match")
```

## 24. While loops
```python
i = 1  
while i < 6:  
  print(i)  
  if i == 3:  
    break  # the loop will stop when i reaches 3
  i += 1
  
  
i = 0  
while i < 6:  
  i += 1  
  if i == 3:  
    continue  #the loop will skip the steps left in the loop for i = 3
  print(i) # 1 2 4 5 6
  

#if the while doesn't respect it's condition anymore, you can use else. this will not be run if while is stopped via the break condition
i = 1  
while i < 6:  
  print(i)  
  i += 1  
else: 
  print("i is no longer less than 6") 
```

## 25. For loops
A [for](https://www.w3schools.com/python/ref_keyword_for.asp) loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string), and it's a bit different from C++, The for loop does not require an indexing variable to set beforehand..
```python
fruits = ["apple", "banana", "cherry"]  
for x in fruits:  
  print(x) 
  
for x in "banana":  
  print(x) #b a n a n a
  
fruits = ["apple", "banana", "cherry"]  
for x in fruits:  
  print(x)  
  if x == "banana":  
    break #stop the loop
    
    
fruits = ["apple", "banana", "cherry"]  
for x in fruits:  
  if x == "banana":  
    continue  #skip one step
  print(x)
  
for x in range(6):  
  print(x) # 0, 1, 2, 3, 4, 5
# we will discuss range later, but note that range(6) is not the values of 0 to 6, but the values 0 to 5.

for x in range(2, 6):  # put like this, parameters show that the range starts from 2 (incl) to 6 (not incl)
  print(x) #2, 3, 4, 5
  
for x in range(2, 30, 3):  #the third parameter represents the increment size
  print(x) # 2, 5, 8, 11, 14, 17, 20, 23, 26, 29
  
for x in range(6):  
  print(x)  
else:  # when the for loop finished (without break) it will execute the else
  print("Finally finished!")
  
#there is also for in for, or a nested for
adj = ["red", "big", "tasty"]  
fruits = ["apple", "banana", "cherry"]  
  
for x in adj:  
  for y in fruits:  
    print(x, y)
"""
red apple  
red banana  
red cherry  
big apple  
big banana  
big cherry  
tasty apple  
tasty banana  
tasty cherry
"""

for x in [0, 1, 2]:  
  pass #if you want an empty for, you need to use `pass`
```