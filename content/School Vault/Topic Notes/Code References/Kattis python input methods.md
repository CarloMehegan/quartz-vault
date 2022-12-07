tags: #python 

1 example of going through all the inputs in a file, and dealing with each one as a separate case
![[Pasted image 20220222171623.png]]
while True:
	try:
		valueString = input()
	except EOFError:
		break

listOfValues = list(map(int, valuesString.split(' ')))


2
![[Pasted image 20220222172323.png]]
line = list(map(int,input().split()))


3
![[Pasted image 20220222172935.png]]
![[Pasted image 20220222173044.png]]
import fileinput
myfile = fileinput.input()


4
```python
import math

tests,totaltime = map(int, input().split())
totaltime = float(totaltime)
secondsneeded = 0

for i in range (tests):
    a,b = map(float, input().split())
    secondsneeded += int(math.ceil(a/b))

if secondsneeded <= totaltime:
    print(0)
else:
    print(math.ceil(secondsneeded/totaltime))
```
taking an input like "3 5" and using map split whatever to split it


5