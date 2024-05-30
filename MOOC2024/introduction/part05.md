# MOOC - Introduction to Python
## Lists within lists

A list can contain another list, or a set of lists:
```python
my_list = [[5, 2, 3], [4, 1], [2, 2, 5, 1]]
print(my_list)
print(my_list[1]) # [4, 1]
print(my_list[1][0]) # 4
```

Since lists aren't constrained to a single data-type, you can create lists which fall under one category:
```python
# storing a collection of data - similar to a database
profiles = [['Lazaro', 26, 1.23], ['Esthel', 26, 3.45]]
```

NB: dictionaries are probably a better way to present this type of data
## Variables and References

Assigning a variable to copy another variable doesn't create a copy as they will have the same reference:
```python
a = [1,2,3]
b = a

a[0] = 100
print(b)

print(id(a)) # 2476857644416
print(id(b)) # 2476857644416
```

The original list can be preserved when copying a list:
```python
if __name__ == "__main__":
    list = [1,3,4,5,6,-3]
    new_list = double_items(list)
    print(list)
    print(new_list)
```

Alternatively, you can replace the list itself:
```python
def x10(my_list: list):
    for i in range(len(my_list)):
        my_list[i] = my_list[i]*10

if __name__ == "__main__":
    list = [1,3,4,5,6,-3]
    x10(list)
    print(list)
```
## Dictionaries
Dictionaries use key-value pairs which are stored in a hash table (referring to areas in the computer's memory):
```python
# use curly braces, keys within []

initialsDict = {}
initialsDict["L"] = "Lazaro"
initialsDict["E"] = "Esthel"

print(len(initialsDict)) # 2
print(initialsDict) # {'L': 'Lazaro', 'E': 'Esthel'}
print(initialsDict["E"]) # Esthel
```
### Keys and Values
* Keys are unique - if a new key is entered, the old value is replaced with the new value:
```python
my_dictionary["suuri"] = "big"
my_dictionary["suuri"] = "large"
print(my_dictionary["suuri"]) # large
```
* Keys must be immutable, so lists can't be used (since they can be changed). This is because they are reduced to a hash value and these are unique.
## Tuples
Similar to lists, except they can use parentheses and are immutable.
```python
def older_people(people: list, year: int):
    older = []
    for person in people:
        if person[1] < year:
            older.append(person[0])
    return older

if __name__ == "__main__":    
    p1 = ("Adam", 1977)
    p2 = ("Ellen", 1985)
    p3 = ("Mary", 1953)
    p4 = ("Ernest", 1988)
    people = [p1, p2, p3, p4]

    print(older_people(people, 1979))
```

Its best to use tuples when there is a set collection of values that are connected in some way, and these values are to be kept constant (which cannot be guaranteed using lists).

 