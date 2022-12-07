Tags: #notes #CSCI100
Created: Saturday, Apr 9

# Using pandas to read CSV
reading a csv
```python
import pandas as pd

data = pd.read_csv("040822 Belarus.csv")

print(data)

```
will print the rows and columns organized

turning csv into a string
```python
import pandas as pd
  
data = pd.read_csv("040822 Belarus.csv")

print(data.to_string())

```
the to_string() command turns it into a string

get a specific column
```python
print(data.Artist)
```
shows the artists

get all the values in one column and make them into a string
```python
s = ""

for i in data.Artist.values:

 s = s + i + "\n"

print(s)
```
s is the string of artists


