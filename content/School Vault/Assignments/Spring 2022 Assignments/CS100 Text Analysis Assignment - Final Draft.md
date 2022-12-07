# CS100 Text Analysis
For this assignment, I analyzed 6 of Dostoevsky's works, centered chronologically around Crime and Punishment. I looked at:
- The House of the Dead (1862)
- Notes from the Underground (1864)
- Crime and Punishment (1866)
- The Idiot (1869)
- Demons (1872)
- The Brothers Karamazov (1880)

My goal was to see if concepts and motifs explored in Crime and Punishment were seen in Dostoevsky's works leading up to it and if these concepts permeated his later works. Many consider Crime and Punishment to be Dostoevsky's magnum opus, and I believe we will see its influence throughout his other works because of how strong of an impact it had.

I started by downloading text files of the six books and formatting them for analysis. I removed the extraneous information at the beginning and end of each book, but left the word "ENDMARKER" at the ends, as it would be useful later for the dispersion plots. In the python script, I took these text files and combined them into one string, keeping the texts in chronological order of when they were released.

### Word Clouds
I used word clouds in order to get a feel for the data and find any trends that were emerging. First, I made a word cloud with all six texts using the default stopwords list.
![[Pasted image 20220410201133.png]]
I kept creating clouds, and with each iteration, I added some of my own stopwords to the list, and finally, I removed Crime and Punishment in order to find what words were most common in the five books that I wasn't familiar with.
![[Pasted image 20220410202221.png]]
From this word cloud, I could start to see what kinds of themes showed up in Dostoevsky's works.
- I am not surprised that 'time' is common, because throughout Crime and Punishment, the time was important to Raskolnikov and the events of the novel all happened within a timeline of a few weeks.
- 'See' might count as a stopword, but it could show how Dostoevsky finds importance in how characters perceive the world around them, and how perceptions and ideologies differ.
- I think that it's strange that 'prince' is the biggest word, but it must be used as an honorific. This surprised me because there is little reference to royalty in Crime and Punishment.

### Dispersion Plots
Next, I split the texts up into tokens. This actually took a long time; I had to wait about ten minutes each time I ran this command. But once I had the text in a tokenized form, I could create text dispersion plots and analyze collocations and concordances.
![[Pasted image 20220410211640.png]]
I wanted to see how themes from Crime and Punishment showed up in the other texts, so I used a dispersion plot to find this. This graph shows all six novels in one timeline. In order to discern where one text ends and the other begins, I left the word 'ENDMARKER' at the end of each book. By tracking the word 'ENDMARKER' in the dispersion plot, we can conveniently split the graph into the six books. Crime and Punishment is the third section, roughly between the 100,000 and 200,000 word markers.

I picked the keywords for the first dispersion plot based on the ones that I thought would be interesting, and based the keywords in the second plot on words I found online in summaries of Crime and Punishment.
![[Pasted image 20220410213642.png]]
I had a few interesting takeaways from these graphs:

Similarities
- The word 'heard' is used very often throughout Dostoevsky's works. I wanted to use this word because the idea of eavesdropping and listening to things you weren't supposed to is Dostoevsky's favorite form of coincidence in Crime and Punishment, and this data shows that listening is important in all of his works.
- 'Money' and 'God' are also common themes throughout Dostoevsky's work, just like in Crime and Punishment.
- St. 'Petersburg' shows up often in Dostoevsky's work as well.

Differences
- The words 'crime' and 'punishment' were not used most often in the actual book Crime and Punishment, but in the stories that came before it. After Crime and Punishment, we can see that they stop showing up as often.
- After Crime and Punishment, the word 'confession' becomes used more often, and 'repent' follows the same trend, but is still used rarely. I believe if I had tracked different versions of these words, like 'repentance' or 'confessing', I could find a more concise answer as to how the idea of repentance was used throughout Dostoevsky's works.
- The word 'illness' is used most often in Crime and Punishment, showing how dramatic Raskolnikov is!

### Collocations and Concordances
Finally, I looked at the top collocations, as well as some concordances for words I was interested in.
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
Names removed:
```
collocations:
every one; old man; young man; great deal; three thousand; old woman;
thousand roubles; hundred roubles; convict prison; next day; long time;
one another; three days; long ago; hard labour; several times
```
There are a few patterns to these collocations: money, time, and punishment. Phrases like 'great deal' and 'thousand rubles' show money's importance, phrases like 'three days,' 'long ago,' and 'next day' show time's importance, and phrases like 'convict prison' and 'hard labour' show punishment. I was not expecting the punishment-related phrases to show up as often as they did.

Finally, I looked at concordances. I chose 'Lazarus' because I have found that the story is referenced in a lot of literary work, and wanted to see if Dostoevsky used it again. I also chose 'split' and 'louse' because they showed up a lot less in the dispersion plots than I thought they would, and wanted to see specifically where they were used.
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
Takeaways:
- Lazarus is only mentioned a couple of times after Crime and Punishment, and the name continues to be used in reference to the story of Lazarus.
- Split doesn't seem to be used with as violent of a connotation as it has in Crime and Punishment.
- Louse is not used until Crime and Punishment, and after Crime and Punishment continues to be used as an emasculating term.

If I were to continue this exploration, I would look at more of Dostoevsky's works, look for different forms of each keyword used in the dispersion plots, and learn more about each of the books in order to draw more informed conclusions.

### Sources
“Books by Dostoyevsky, Fyodor.” _Project Gutenberg_, https://www.gutenberg.org/ebooks/author/314. Accessed April 10, 2022.

Shmoop Editorial Team. “Crime and Punishment Themes.” _Shmoop_, Shmoop University, 11 Nov. 2008, https://www.shmoop.com/crime-and-punishment/themes.htmlAnalysis. Accessed April 10, 2022.