Tags: #python 
Created: Sunday, Feb 27

# Python commands

### Welcome
A page for commands that are common in python and good to know the use of

### Commands
min(): returns the lowest value
```python
min()

#ex 1
x = min(5, 10)

#ex 2
a = (1, 5, 3, 9)  
x = min(a)
```

split(): splits a string into a list of strings, separated by default at whitespace.
```python
aString.split()

#1
x = aString.split(',')

#2
total = 0
for number in input().split():
    total += int(number)
print(total)

#2.5
print(sum(int(number) for number in input().split()))

```

strip(): removes whitespace at the beginning and end of a string