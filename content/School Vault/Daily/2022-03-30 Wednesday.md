Tags: #daily #flashcards/todo

### Wednesday, Mar 30

calc
starting chapter 11 sequences and series


ling
summer class prof cochrane is teaching looks interesting
English Language and US Culture
[[Meaning II]]
[[Reflection - Class Contribution]]


cs
- visual analysis due tonight
- quiz this weekend on anastasia and stuff from this week
- [[Tufte - The Visual Display of Quantitative Information]]
- [[Anastasia & Visual Analysis]]
- module 5 notebook - More on Word Clouds

#python
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