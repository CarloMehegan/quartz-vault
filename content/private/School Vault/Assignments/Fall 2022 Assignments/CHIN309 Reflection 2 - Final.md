## CHIN309 Reflection 2 - Distant Reading of Tang Poetry
Carlo Mehegan
October 21, 2022

##### Goals
In class we analyzed poetry from the Tang Dynasty through close reading. My goal for this reflection was to take a large collection of Tang poetry and analyze it through distant reading by looking at word frequency.

##### Finding poems
I wanted to find a large collection of Tang poetry, in .txt form, containing the poets we discussed in class. Fortunately I was able to find a collection quickly called *Three Hundred Tang Poems*. Project Gutenberg had a .txt version in Chinese and an audio version with an English table of contents. Using the English table of contents (and Google Translate), I found that this work contained some of the poets we discussed in class, such as Li Bai, Du Fu, and Wang Wei. I downloaded the .txt and cut it down to just the poems to create the data set.

##### Making the wordclouds
I started by running the poems through a script to create a wordcloud showing the most frequent strings of characters as larger. The first wordcloud I created was to make sure the script was working.

![[Pasted image 20221022230416.png]]

I wasn't able to discern much from this graphic. The wordcloud was showing the most frequent combinations of characters instead of the most frequent characters. So next, I split the .txt file by character and made another wordcloud.

![[Pasted image 20221022231246.png]]

Removing collocations, reducing number of characters shown to 100:

![[Pasted image 20221022232153.png]]

This graphic was more useful, but at this point I realized I don't speak Chinese, so I needed a way of translating these characters. To do this, I made another script that printed the most frequent characters along with how many times they appeared.

```
100 most common characters and their frequencies

[('，', 1580), ('。', 1321), ('作', 351), ('者', 346), ('：', 322), ('不', 222), ('人', 214), ('山', 175), ('1', 172), ('0', 170), ('2', 163), ('？', 151), ('無', 134), ('一', 133), ('月', 130), ('日', 127), ('；', 123), ('夜', 120), ('天', 120), ('風', 117), ('白', 117), ('長', 112), ('來', 105), ('雲', 104), ('上', 102), ('有', 98), ('春', 95), (7', 94), ('何', 92), ('行', 92), ('之', 91), ('生', 91), ('君', 90), ('李', 87), ('中', 87), ('水', 87), ('見', 85), ('花', 85), ('時', 84), ('王', 84), ('3', 83), ('下', 79), ('青', 79), ('歸', 78), ('如', 78), ('秋', 75), ('明', 72), ('萬', 72), ('三', 71), ('為', 71), ('落', 71), ('空', 70), ('自', 67), ('此', 64), ('金', 63), ('雨', 63), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9', 62), ('去', 62), ('今', 61), ('馬', 60), ('南', 59), ('杜', 59), ('城', 59), ('欲', 59), ('家', 58), ('將', 58), ('西', 58), ('古', 58), ('年', 58), ('未', 57), ('子', 57), ('門', 57), ('在', 56), ('心', 56), ('清', 56), ('飛', 56), ('寒', 56), ('聲', 56), ('客', 55), ('事', 54), ('處', 54), ('別', 54), ('朝', 54), ('高', 53), ('陽', 53), ('黃', 52), ('玉', 51), ('大', 51), ('入', 50), ('與', 50), ('出', 50), ('道', 50), ('望', 49), ('十', 49)]

Ran through Google Translate

[(',', 1580), ('.', 1321), ('do', 351), ('who', 346), (':', 322), ('no', 222), ( 'person', 214), ('mountain', 175), ('1', 172), ('0', 170), ('2', 163), ('?', 151), ('none ', 134), ('one', 133), ('month', 130), ('day', 127), (';', 123), ('night', 120), ('day', 120), ('wind', 117), ('white', 117), ('long', 112), ('come', 105), ('cloud', 104), ('on', 102) , ('you', 98), ('spring', 95), ('jiang', 95), ('xiang', 94), ('he', 92), ('line', 92), ( 'zhi', 91), ('sheng', 91), ('jun', 90), ('li', 87), ('zhong', 87), ('water', 87), ('see ', 85), ('flower', 85), ('time', 84), ('king', 84), ('3', 83), ('lower', 79), ('green', 79), ('Return', 78), ('Ru', 78), ('Autumn', 75), ('Ming', 72), ('Wan', 72), ('Three', 71) , ('wei', 71), ('fall', 71), ('empty', 70), ('si', 67), ('this', 64), ('jin', 63), ( 'rain', 63), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9 ', 62), ('go', 62), ('now', 61), ('ma', 60), ('nan', 59), ('du', 59), ('city', 59), ('desire', 59), ('home', 58), ('will', 58), ('west', 58), ('ancient', 58), ('year', 58) , ('wei', 57), ('zi', 57), ('door', 57), ('zai', 56), ('xin', 56), ('clear', 56), ( 'Fly', 56), ('Cold', 56), ('Sound', 56), ('Guest', 55), ('Thing', 54), ('Location', 54), ('Don't ', 54), ('towards' , 54), ('High', 53), ('Yang', 53), ('Yellow', 52), ('Jade', 51), ('Big', 51), ('In', 50 ), ('and', 50), ('out', 50), ('dao', 50), ('look', 49), ('ten', 49)]
```

Next, I spent a while trying to format the data to make a graph (with the first two most common characters, the comma and period, removed):

![[Pasted image 20221022191816.png]]

Then I realized that some of the characters in the list were from the names of the authors, which got left in the dataset. I also realized that Google Translate was combining some of the characters and the translation was fluctuating from instance to instance, so I added periods between each word in the word list and translated it in sections, making sure I got 100 English words to match the 100 characters. Eventually, I had this list:

```
[('，', 1580), ('。', 1321), ('不', 222), ('人', 213), ('山', 175), ('1', 172), ('0', 170), ('2', 163), ('？', 151), ('一', 133), ('無', 133), ('月', 130), ('日', 127), ('；', 123), ('夜', 120), ('天', 120), ('風', 117), ('來', 105), ('雲', 104), ('上', 102), ('長', 101), ('有', 98), ('江', 95), ('春', 94), ('相', 94), ('何', 92), ('行', 92), ('生', 91), ('君', 90), ('之', 88), ('水', 87), ('中', 86), ('見', 85), ('花', 85), ('時', 84), ('3', 83), ('下', 79), ('青', 79), ('歸', 78), ('如', 78), ('白', 77), ('秋', 74), ('明', 72), ('萬', 72), ('三', 71), ('落', 71), ('為', 70), ('自', 67), ('空', 67), ('此', 64), ('雨', 63), ('金', 62), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9', 62), ('去', 62), ('今', 61), ('南', 59), ('城', 59), ('欲', 59), ('家', 58), ('將', 58), ('馬', 58), ('古', 58), ('年', 58), ('未', 57), ('門', 57), ('西', 57), ('在', 56), ('心', 56), ('清', 56), ('飛', 56), ('寒', 56), ('子', 56), ('聲', 56), ('客', 55), ('事', 54), ('處', 54), ('別', 54), ('朝', 54), ('陽', 53), ('黃', 52), ('高', 51), ('大', 51), ('入', 50), ('與', 50), ('玉', 50), ('出', 50), ('道', 50), ('望', 49), ('十', 49), ('流', 49), ('二', 48), ('歌', 48), ('送', 48), ('宮', 48), ('得', 47)]

Just the characters

，. 。. 不. 人. 山. 1. 0. 2. ？. 一. 無. 月. 日. ；. 夜. 天. 風. 來. 雲. 上. 長. 有. 江. 春. 相. 何. 行. 生. 君. 之. 水. 中. 見. 花. 時. 3. 下. 青. 歸. 如. 白. 秋. 明. 萬. 三. 落. 為. 自. 空. 此. 雨. 金. 4. 5. 6. 7. 8. 9. 去. 今. 南. 城. 欲. 家. 將. 馬. 古. 年. 未. 門. 西. 在. 心. 清. 飛. 寒. 子. 聲. 客. 事. 處. 別. 朝. 陽. 黃. 高. 大. 入. 與. 玉. 出. 道. 望. 十. 流. 二. 歌. 送. 宮. 得.

Passing through Google Translate, removing punctuation and arabic numerals:

No. People. Mountains. One. No. Month. Sun. Night. Sky. Wind. Comes. Cloud. Up. Long. There is. River. Spring. Phase. What. Travel. Life. Jun. Of. Water. Middle. See. Flower. Time. Down. Green. Returning. Such as. White. Autumn. Ming. Wan. Three. Fall. For. From. Empty. This. Rain. Gold. Go. Today. South. City. Desire. Home. Will. Horse. Ancient. Year. Not. Door. West. In. Heart. Clear. Flying. Cold. Son. Sound. Guest. Things. Where. Don't. Facing. Yang. Yellow. High. Big. Entering. And. Jade. Out. Dao. Hope. Ten. Stream. Two. Song. Send. Palace. Get.
```

##### Themes
These translations are not perfect due to the nature of Google Translate, but I believe they accurately convey the themes present throughout the 300 analyzed poems. 

One prominent theme is nature, seen through words like Sun, Night, Sky, Wind, Cloud, Green, Autumn, and Horse. We first found this theme prevalent in poetry from the Six Dynasties Period, and it isn't surprising that it continues to show in this dynasty. This also matches the writing we analyzed in class, like the nature descriptions Du Fu uses in poems like *A Song on How My Thatched Roof Was Ruined by the Autumn Wind*. It's also interesting that the word Mountain is the third highest word in the frequency list, and I'm still unsure why.

Another prominent theme is the passage of time, seen through words like Month, Year, Ancient, Today, Sun, Night, Autumn, Long, Time. We didn't see this theme appear in the poetry we read in class. Another thing that surprises me is that there are no words related to alcohol or drinking, because it was a common theme in Li Bai's work. The Dao is also mentioned more often than I expected, showing up 50 times. We discussed Daoism in class, and it was interesting to see it show up in these poems. I wondered if the Dao was being mentioned throughout the data or if there were one or two poets thatfocused on Daoism. I looked through the data for mentions of "道" and they were relatively spread out. The poems are organized by author for the most part, meaning that the data must be from more than just a few of the poets.

There are also words like Travel, City, Gold, Jade, and Palace, which reflect the fact that many of the people who wrote poems were wealthy or came from rich households. Poetry was a very respected form of writing, and almost all poets were educated and literate with many of them serving in the government.

Overall, the most frequent words typically matched what I expected, and gave further insight into the poetry of the Tang Dynasty. If I could continue this analysis, I would want to add more poems to my data set and dive further into the use of specific words like Dao. I could also improve the accuracy of this analysis with the help of a Chinese speaker and a deeper understanding of Chinese history.

##### Sources
_唐诗三百首 by Hengtangtuishi_. (2016, June 13). Project Gutenberg. https://www.gutenberg.org/ebooks/52323. Accessed Oct. 22, 2022.

_Three Hundred Tang Poems, Volume 1 by Various_. (2007, April 4). Project Gutenberg. https://www.gutenberg.org/ebooks/20968. Accessed Oct. 22, 2022.

‌amueller. (2022, October 18). _amueller/word_cloud: A little word cloud generator in Python_. GitHub. https://github.com/amueller/word_cloud. Accessed Oct. 22, 2022.

_create wordcloud with chinese — wordcloud 1.8.1 documentation_. (2020). Github.io. https://amueller.github.io/word_cloud/auto_examples/wordcloud_cn.html. Accessed Oct. 22, 2022.

‌