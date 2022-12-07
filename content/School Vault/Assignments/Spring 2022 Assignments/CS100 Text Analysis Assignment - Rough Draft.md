Tags: #assignment #CSCI100
Created: Sunday, Apr 10

# CS100 Text Analysis - Rough Draft

### Prompt

**Text Analysis Assignment**
**Submit before midnight, 4/10/2022**
You have read several texts in this class in close reading, and we have discussed how computers read text in order to explore how they might be used for distant reading. In this assignment, you will use the computational tools we have seen in class to analyze a text of your choosing related to Russia. Read what follows closely.

**Text selection**

Select a text of at least 1500 words related to Russia – longer texts will be more interesting for analysis. The text does not have to be in Russian, but it can be. Some text sources to consider:

Gutenberg Project - for literary texts/literary criticism

BBC News (in Russian/in English)

WM Library Catalog 

Consider the format of your text, and how you will reframe it as data that the computer can read. You could copy-paste from the web into a text file, or you could take a screenshot or download to .pdf and read the text in with optical character recognition (tesseract on JupyterHub). 

**Programming Assignment**

The programming portion of the assignment will make use of the tools we have explored in class, fundamental programming as well as NLTK and wordclouds. Make use of the materials from class. **We expect for you to have MANY QUESTIONS for Francis** – come talk to us, do not know how to start, get an error you don’t understand, need clarification or have difficulties that you can’t resolve on your own.

You will submit a Python script (a .py file) that does the following – please read carefully as you have choices for some of the tasks:

• Reads in your text from a file – this may be all of the text at once or line by line depending on how you choose to proceed

• Divides the text into tokens (word, sentences, or other structures as appropriate) and count the number of words, as well as the number of unique words

• Performs linguistic analysis to include word frequencies (top ten words) and at least ONE of the following: collocations, concordances of the most frequent word(s), common contexts of the most frequent word(s); think carefully about any words that you may want to exclude in your analysis

• Creates at least TWO figures, which may include (but could include others): a Wordcloud, a Frequency Distribution plot, a Dispersion plot

**Deliverable (what you turn in: 3 documents as a bundle)**

• A .py file (not a notebook) containing your code. Please make use of code we have given you. It is fine to copy and paste. Your code should be organized so that it is easy to follow and we can trace your steps. Include comments to help explain what you did.

• Your source text. If this is a .txt file, upload that. If it is a .png or .pdf, upload that. If you used some other format or mechanism (i.e. Python requests) indicate that. We should be able to run your code using whatever your source you provide.

• A one page .pdf document containing:

o A 250 words essay describing what you did and what you found in the text. This exercise is exploratory, so you may not have had a specific question going into it, but you should detail what you found by doing your analysis, and any conclusions you can draw about the text, as well as any difficulties you encountered, and any further information you would have liked to have had. Be sure to include things you calculated, such as the total word count and the unique word count. Refer to your figures as needed. This is the first page.

o The accompanying figures for your analysis.

o A citation for the source of your text (MLA format) and any other sources you used.

---

### Plan
Text: brothers karamazov or maybe all of dostoevsky works i can find on project gutenberg
- 1862 The House of the Dead
- 1864 Notes from the Underground
- 1866 Crime and Punishment
- 1869 The Idiot
- 1872 Demons
- 1880 The Brothers Karamazov
These are the books published before and after crime and punishment, and I will see how themes from crime and punishment developed and persisted in Dostoevsky's other works.

Keywords: ill use the words like "axe" "split" "murder" "crime" "st petersburg" that we used for [[Crime and Punishment]] and see how those words show up in dostoevskys other works? this is good enough i guess
- axe
- split
- murder
- crime
- punishment
- petersburg
- confession
- eavesdrop
- listening

Programming:
- [x] Divide text into words
- [x] Collocations
- [x] Word cloud
- [x] Dispersion plot

Deliverables:
- [x] python file
- [x] text file
- [x] write up document
	- [x] 250 words on what you did, what you found, what you were looking for, stats
	- [x] figures pasted
	- [x] citations


# progress
step 1 making the txt file ill just download all the dostoevsky works i can find
ok did it and made a wordcloud with just these 6 books:
![[Pasted image 20220410201133.png]]
and if we take out crime and punishment:
![[Pasted image 20220410201256.png]]
these are done using basic stopword removal, now to get rid of more:
'one', 'though', 'said', 'say', 'shall', 'could', 'thought', 'know', 'tell', 'even'
![[Pasted image 20220410201804.png]]
add a few more stopwords to the list:
'come', 'go', 'like', 'well', 'went', 'yet', 'let', 'still', 'must', 'man', 'day'
![[Pasted image 20220410202221.png]]
interesting words here
prince - not sure why this is used the most, must be used as an honorrific
see - could be a stopword, but sight may be an important motif
time - makes sense to me that time is something on Dostoevsky's mind often
Alyosha - who is that?

other notes
money is about as big as the word love is
the word word is pretty big
nothing is big also, could mean poor, or no morals, etc, also a theme for Dostoevsky

honestly there isn't much here, so i want to now look at keywords from crime and punishment. with a dispersion graph, we can see how frequently words are used over time, and the text that NLTK is using has the six works in chronological order.
I expect to see the words used often in the middle where crime and punishment would be, and we may see clusters close to crime and punishment

![[Pasted image 20220410211640.png]]
and part two
![[Pasted image 20220410213642.png]]
sick

```
collocations:
Stepan Trofimovitch; Pyotr Stepanovitch; Varvara Petrovna; Katerina
Ivanovna; Nikolay Vsyevolodovitch; Fyodor Pavlovitch; Nastasia
Philipovna; Yulia Mihailovna; every one; Lizabetha Prokofievna;
Mavriky Nikolaevitch; old man; Avdotya Romanovna; Evgenie Pavlovitch;
Dmitri Fyodorovitch; Pulcheria Alexandrovna; Pyotr Petrovitch; young
man; great deal; three thousand; old woman; Mrs. Epanchin; thousand
roubles; Rodion Romanovitch; Nikolay Parfenovitch; Madame Hohlakov;
Andrey Antonovitch; hundred roubles; Alexey Fyodorovitch; Father
Zossima; Lizaveta Nikolaevna; convict prison; Sofya Semyonovna; Pyotr
Ilyitch; Marya Timofyevna; Gavrila Ardalionovitch; Father Païssy; next
day; Porfiry Petrovitch; long time; one another; Nina Alexandrovna;
Marfa Petrovna; three days; long ago; Darya Pavlovna; hard labour;
Sofya Matveyevna; Ippolit Kirillovitch; several times
```

concordances:
```
Displaying 10 of 10 matches:
Porfiry “ And ... do you believe in Lazarus ’ rising from the dead ” “ I ... I 
r the pages “ Where is the story of Lazarus ” he asked suddenly Sonia looked ob
the table “ Where is the raising of Lazarus Find it for me Sonia. ” She stole a
 “ Now a certain man was sick named Lazarus of Bethany ... ” she forced herself
d spoken He cried with a loud voice Lazarus come forth “ And he that was dead c
 “ That is all about the raising of Lazarus ” she whispered severely and abrupt
m which she had read the raising of Lazarus to him At first he was afraid that
ver it at the last He who called to Lazarus ‘ Lazarus come forth ’ and the dead
the last He who called to Lazarus ‘ Lazarus come forth ’ and the dead man lived
 in the parable of the rich man and Lazarus and beholds heaven and can go up to


Displaying 8 of 8 matches:
up a row Says he to Aukoudim 'Let 's split the difference Give me back my four
manticism that they would all simply split their sides with laughter and that t
 that I shall strike her on the head split her skull open ... that I shall trea
the sharp edge just on the skull and split at one blow all the top of the head
ng us about old times till we nearly split our sides .... Especially how he onc
solitude All mankind in our age have split up into units they all keep apart ea
are you shouting for D ’ you want to split your throat ” he said addressing Vru
the flooring pulled apart the planks split up all the gallery I am told He is s


Displaying 10 of 10 matches:
ly towards him and that we ought to repent our uselessness Our work consisted
least have been life But he did not repent of his crime At least he might have
nks alone and go into the desert to repent Or why not become a monk himself Th
 be guilty and fearing both sides I repent of what I had no share in my circum
 and if it 's true we induce him to repent of it and if he gives us his word o
-day with my revolver not because I repent and am afraid of you but because wh
me to get sleep enough much less to repent of one ’ s sins While you have deni
h hatred as he went out “ I don ’ t repent shedding your blood ” he cried “ Be
in these days to find a man who can repent of his stupidity and publicly confe
next world old Kuzma must sincerely repent of his past relations with Grushenk


Displaying 17 of 17 matches:
 I shall always be insulted by every louse that is my doom And what is it to me
existence No more than the life of a louse of a black-beetle less in fact becau
I too want .... Ech I am an æsthetic louse and nothing more ” he added suddenly
like a madman “ Yes I am certainly a louse ” he went on clutching at the idea g
a And what shows that I am utterly a louse ” he added grinding his teeth “ is t
ps viler and more loathsome than the louse I killed and _I felt beforehand_ tha
th Good God ” “ I ’ ve only killed a louse Sonia a useless loathsome harmful cr
ful creature. ” “ A human being -- a louse ” “ I too know it wasn ’ t a louse ”
a louse ” “ I too know it wasn ’ t a louse ” he answered looking strangely at h
ed myself whether a human being is a louse it proved that it wasn ’ t so for me
out then and quickly whether I was a louse like everybody else or a man Whether
e that path because I am just such a louse as all the rest He was mocking me an
w Welcome your guest If I were not a louse should I have come to you Listen whe
rhaps after all I am a man and not a louse and I ’ ve been in too great a hurry
 done from humanity She wasn ’ t ‘ a louse ’ you know ” he pointed to the corne
reast Nikolay Vsyevolodovitch Even a louse may be in love and is not forbidden
or all the world like a filthy human louse -- that 's how I look on you You 've
```