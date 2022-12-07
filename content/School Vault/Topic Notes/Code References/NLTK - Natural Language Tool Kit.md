Tags: #flashcards #CSCI100
Created: Wednesday, Mar 2

# Natural Language Processing with NLTK
NLTK is a python library for natural language processing
Stands for Natural Language Tool Kit

Stemming
- remove modifiers of words like running vs. run
- leaves just the root words
- [[Morphology I#Bound and Free Morphemes]] wow strangely relevant


imports for the following examples
```python
import string
from nltk.tokenize import word_tokenize

import nltk
nltk.download('stopwords')
from wordcloud import WordCloud
import matplotlib.pyplot as plt
from nltk.corpus import stopwords

```


Collocations = a two word phrase, or a pair of words that are used together frequently
```python
tokens = word_tokenize(cp) #cp is the name of the string youre using
tokens = [token for token in tokens if token not in string.punctuation] #remove .,! etc
text = nltk.Text(tokens) #create Text object

text.collocations(40)

#output:
"""Katerina Ivanovna; Pyotr Petrovitch; Pulcheria Alexandrovna; Avdotya
Romanovna; Rodion Romanovitch; Marfa Petrovna; Sofya Semyonovna; old
woman; Porfiry Petrovitch; Amalia Ivanovna; great deal; Nikodim
Fomitch; young man; Ilya Petrovitch; Andrey Semyonovitch; Hay Market;
Dmitri Prokofitch; Good heavens; police station; Yes yes; head clerk;
stood still; police office; dear fellow; thousand roubles; long ago;
Arkady Ivanovitch; Semyon Zaharovitch; Good God; make haste; Mr.
Luzhin; Praskovya Pavlovna; one another; Alyona Ivanovna; Mr.
Lebeziatnikov; ten minutes; run away; next day; several times; long
time"""
```

Concordance
```python
tokens = word_tokenize(cp) #cp is the name of the string youre using
tokens = [token for token in tokens if token not in string.punctuation] #remove .,! etc
text = nltk.Text(tokens) #create Text object

text.concordance('time')

#output
"""
e lived on the floor below and every time he went out he was obliged to pass h
which invariably stood open And each time he passed the young man had a sick f
ject quite the contrary but for some time past he had been in an overstrained 
im and not caring to observe it From time to time he would mutter something fr
ot caring to observe it From time to time he would mutter something from the h
om indeed he disliked meeting at any time And yet when a drunken man who for s
en he had been lost in dreams At the time he had put no faith in those dreams 
h only I did not notice it the other time ” he thought with an uneasy feeling
"""
```

Dispersion plot
```python
tokens = word_tokenize(cp) #cp is the name of the string youre using
tokens = [token for token in tokens if token not in string.punctuation] #remove .,! etc
text = nltk.Text(tokens) #create Text object

text.dispersion_plot(['Katerina', 'Pyotr', 'Pulcheria', 'police', 'Raskolnikov', 'Sofya', 'Lazarus', 'axe'])
```
![[Pasted image 20220302163319.png|400]]

---
nltk start code
example from class (notebook name: "more on wordclouds")
```python
import nltk

nltk.download('stopwords')

from wordcloud import WordCloud
import matplotlib.pyplot as plt
from nltk.corpus import stopwords

dost = open('crime_and_punishment.txt', 'r', encoding = 'UTF-8') 
cp = dost.read()
dost.close()
wordcloud = WordCloud(collocations = False).generate(cp)
plt.figure(figsize=[10,10])
plt.imshow(wordcloud)
plt.axis('off')
plt.show()

```




### Text analysis assignment w/ NLTK

##### code snippets from class
[[2022-03-30 Wednesday]]

Creating a word cloud using a mask
first run these
```
!pip install wordcloud
!pip install nltk

```

code for
- importing the right tools
- adding stopwords
- making word cloud
- adding mask
- generating masked word cloud
```python
import nltk
nltk.download('stopwords')

from wordcloud import WordCloud
import matplotlib.pyplot as plt
from nltk.corpus import stopwords


stops = stopwords.words('english')
print(stops)
stops.append('would')
#how do we add things?
#what should we add?


# use crime and punishment as base text
dost = open('crime_and_punishment.txt', 'r', encoding = 'UTF-8') 
cp = dost.read()
dost.close()


# code for making the word cloud
wordcloud = WordCloud(colormap='Pastel2', background_color='Red', stopwords = stops).generate(cp) #make the wordcloud
plt.figure(figsize=[10,10]) #change figure size
plt.imshow(wordcloud) #show wordcloud
plt.axis("off")#get rid of x and y axes
plt.show()

#--------------------------------------------------------------------------

# using a mask
from PIL import Image
import string
from imageio import imread


def make_mask(input_file, output_file = 'mask.png', invert = False, cutoff = 128):
    image_file = Image.open(input_file)
    image_file = image_file.convert('L') # convert image to black and white
    image_file.mode = 'L'
    #to invert
    if invert:
        image_file = image_file.point(lambda x: 0 if x>cutoff else 255)
    #no inversion
    else:
        image_file = image_file.point(lambda x: 0 if x<cutoff else 255)
    image_file.save(output_file)
    return imread(output_file)

mask = make_mask('axe.png')
mask
print()

# generate the masked word cloud!
dost = open('crime_and_punishment.txt', 'r', encoding = 'UTF-8') 
cp = dost.read()
dost.close()
wordcloud = WordCloud(mask = mask, background_color='white', stopwords = stops,
                     contour_color = 'grey', contour_width = 0.5).generate(cp)
plt.figure(figsize=[10,10])
plt.imshow(wordcloud)
plt.axis('off')
plt.savefig('axe_cloud.png')
plt.show()



# another mask
mask2 = make_mask('church.png', 'mask2.png', cutoff = 200)
Image.open('mask2.png')

dost = open('crime_and_punishment.txt', 'r', encoding = 'UTF-8') 
cp = dost.read()
dost.close()
wordcloud = WordCloud(mask = mask2, background_color='white', stopwords = stops,
                     contour_color = 'grey', contour_width = 0.5).generate(cp)
plt.figure(figsize=[10,10])
plt.imshow(wordcloud, interpolation = 'bilinear')
plt.axis('off')
plt.savefig('axe_cloud.png')
plt.show()


```












