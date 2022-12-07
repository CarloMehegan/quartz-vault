```python
import nltk

nltk.download('punkt')

from nltk import word_tokenize, sent_tokenize

  

#Read in the text from the excerpt from Notes From Underground

with open('notes_from_underground_excerpt.txt', 'r', encoding = 'UTF-8') as file:

 nu = file.read()

  

#Ask the user if they would like to tokenize by words or sentences

#The default is by words, do this unless they specifically respond with SENTENCE to the prompt

choice = input('Enter SENTENCE to tokenize by sentence, or enter any other text to tokenize by words: ')

how_many = int(input('How many tokens would you like to print? Printing will start with the first token. \

Enter an integer greater than 0: '))

  

#use a conditional  - try to reduce repeated code....be clever!

#For both cases (whether it is word or sentence)

#print out how many total tokens there are in the format: 100 total tokens

#print out how many unique tokens there are in the format: 100 unique tokens

#print out the first how_many tokens (just print them as a list with no additional text)

  

if choice == "SENTENCE":

 nu = sent_tokenize(nu)

else:

 nu = word_tokenize(nu)

  

print(len(nu), "total tokens")

this_many = nu[:how_many]

nu = set(nu)

print(len(nu), "unique tokens")

print(this_many)
```
code from a cs100 assignment