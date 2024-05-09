# MOOC - Introduction to Python
## Returning vs Printing values

`return` allows for the evaluation of an expression to be used in a function:
```python
def printmax(a, b):
    if a > b:
        print(a)
    else:
        print(b)

def returnmax(a, b):
    if a > b:
        return a
    else:
        return b

def sum(x,y):
    print(x+y)

sum(printmax(14,2), 6) # this won't work
sum(returnmax(14,2), 6) # this will work
```
## Lists

Items within a list are mutable (i.e., they can be changed):
``` python
my_list = [0,0,2,3,4,5]
print(my_list) # prints list above
my_list[1] = 1
print(my_list) # prints [0,1,2,3,4,5]
```
### Appending and Inserting 

The `append` method adds items to the end of a list:
```python
list = []
items = int(input("How many items: "))

for i in range(items):
    list.append(int(input(f"Item {i+1}: ")))
print(list)
```

The `insert` method adds items within a specific index - *NB: this doesn't replace an item*:
```python
my_list = [0,0,2,3,4,5]
print(my_list) # prints list above
my_list.insert(1, 100) # syntax is (index, item)
print(my_list) # prints [0,100,0,2,3,4,5]

# The indexes of the numbers to the right of the inserted item are 'pushed' down one.
```
### Removing and Popping

If you know the *index* of an item, you can `pop` it using it's index:
```python
my_list = [2,4,5,6]
popped = my_list.pop(0) # this pops whatever is at index 0.
print(my_list)
print(popped)
```

If you know the *value* of an item, you can `remove` it using it's value:
```python
my_list = [1,2,3,2,5]
print(my_list)
my_list.remove(2) # like the find method, this affects the first instance of an item
print(my_list) # [1,3,2,5]
```

### Sorting Lists

You can sort lists using a method, or a function:
```python
list = [4,2,1,3,5]
list.sort()
print(list) # modifies original list so that the items are ordered.

list2 = [4,2,1,3,5]
print(sorted(list2)) # returns a sorted version of list2
print(list2) # to show that list2 hasn't been modified
```
### Min, Max, Sum

All are functions and work as expected:
```python
list = [5,3,1,4,2]

small = min(list)
big = max(list)
total = sum(list)

print(f"{small}, {big}, {total}")
```

## Definite iteration

The `for` loop syntax allows you to loop through several iterable objects (e.g., a string or a list):
```python
list = [1,2,3,4,5]
string = "Lazaro"

for item in list: # item is just a placeholder - it doesn't matter what it's called
	print(item)

for character in string:
	print(character)
```
### Range syntax

The main features of range(a, b, c) are:
* a: start
* b: stop (exclusive, i.e., it is b-1)
* c: step (increment)
	* NB: The step can also be negative

A range is not a list, but can be converted into one.

## Print Formatting

f-strings can be used to format strings, and round decimals:
```python
number = 1/3
print(f"The number is {number}") # 0.333333333333333
print(f"The number is {number:.2f}") # 0.33
```
