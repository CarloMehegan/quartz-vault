My answer:
```python
#looping
while True:
	#try to get an input, stops when we reach the last input
	#EOFError means "end of file error"
	try:
		valuesString = input()
	except EOFError:
		break
	
	#input is a string of numbers separated by spaces, ex. "1 2 3"
	#takes the string, creates a list
	#the map function takes the string of numbers and 
		#the int part of the paramenter is the function that map will take on the second parameter
		#the second parameter is an iterable, the split command returns splits the string of numbers into
			#an iterable with a string for each number
		#the map function applies the int function to every string in the list created by valuesString.split
		#so basically it just makes a new iterable where the strings are now integers
	#finally, we turn the map into a list
	listOfValues = list(map(int, valuesString.split(' ')))
	#print (listOfValues)

	#we need to return which number in the list is the sum of the other numbers
	#the sum of every number in the list, including the sum of the other numbers, will be even always
	#just take the sum and divide by 2
	answer = int( sum(listOfValues) / 2 )
	print(answer)

```

Someone else's answer: from [[Kattis python input methods]]
![[Pasted image 20220222171623.png]]

