# MOOC - Introduction to Python
## Loops with conditions

`while` can be used with Boolean expressions:
```python
ul = int(input("Upper Limit: "))
n = 1

while n <= ul:
    print(n)
    n *= 2;
```
### Loops using break and continue
*  `continue` will cause the loop to restart from the beginning of the loop
*  `break` breaks the loop
*  Within nested loops, `break` only 'breaks' the innermost loop.

```python
n = int(input("Please type in a number: "))
left = 1

while left <= n:
    right = 1
    while right <= n:
        print(f"{left} x {right} = {left * right}")
        right += 1
    left += 1
```

## Strings: len() and indexing

* `len()` works like it does in SQL
*  Indexing is zero based, and you can index into a string (since a string is an array of chars).
*  You can use negative indexing to start from the last char in the string. This starts from -1.

```python
h = "hello there"
print(len(h)) # returns 11, as len() includes whitespace
print(h[4]) # returns 'o'
print(h[-1]) # returns 'e'
```
## Substrings and slices
* To extract a substring that you know the index position of, use notation `[a:b]`
* The substring starts at `[a:` but ends before `b]`:
```python
a = "hello"

print(a[0]) # "h"
print(a[2:4]) # "ll"
print(a[:3]) # defaults to 0, so "hel"
print(a[2:]) # defaults to end of string, so "llo"
```

* You can check for a substring in a string by using the `in` operator, which returns a Boolean expression:
```python
s = "yippee"

print("y" in s) # True
print("ippe" in s) # True
print("iy" in s) # False
print("eee" in s) # False
```
## Method Calls
Functions are written prior to the object, like how `len()` is written before `x` in `len(x)`. Methods, on the other hand, attach to the object:
```python
s = "dictionary"
s.find("tion") # find() is a method call, which attaches to object 's'
```
## Defining Functions
You can create your own functions, like `len()`, `str()`, by defining them:
```python
def seven_brothers():
    print("""Aapo
    Eero
    Juhani
    Lauri
    Simeoni
    Timo
    Tuomas""")
if __name__ == "__main__":
	seven_brothers()
```

### Arguments and parameters
In defining a function, you use parameters for placeholders:
```python
'''
the function heythere takes 'name' as a parameter, which is a placeholder for whatever value you eventually place there. It also indicates that it expects one argument (since there is one parameter).
'''

def heythere(name):
	print("Hey," + name)

heythere("Laz")
```

You can also use an `if` statement while you're defining the function:
```python
def greeting(name):
	if name == "Mum":
		print("Hello ma")
	else:
		print(f"Hi, {name}")

greeting("Mum")
greeting("Jake")
```
