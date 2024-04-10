# MOOC - Introduction to Python
Conditions, Loops
## More on conditionals
`if`, `elif`, and `else` are similar to a `case` statement, in which you can have multiple `elifs`, then end with an `else` statement:
```
if n > 20:
	print("over 20")
elif n > 10:
	print("over 10")
else:
	print("under 10");
```

NB: 
* `else` is optional
* `not` is used in negation
* You can chain conditions: `a < b <= c`
## Loops
### Basic Loop
`while True` will create a loop, running the loop until broken. NB: `break` doesn't necessarily turn `True` into `False`, it just breaks the loop:  

```
attempts = 0
while True:
    pin = int(input("PIN: "))
    attempts += 1
    if pin == 4321:
        if attempts == 1:
            print(f"Correct! It only took you one single attempt!")
            break
        else:
            print(f"Correct! It took you {attempts} attempts")
            break
    print("Wrong")
```
### Helper variables
A helper variable can be used to store last input or build a string of inputs. In this example, I used one variable (`story`)  to keep adding the input, concatenated by a comma. I also used another variable (`lastword`) to keep the last inputted word:
```
story = ""
lastword = ""

while True:
    word = input("Please type a word: ")
    if word == 'end':
        print(f"{story}")
        break
    if word == lastword:
        print(f"{story}")
        break
    story += word + " "
    lastword = word
```
