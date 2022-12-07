tags: #notes #topic
creation date: [[2022-10-12 Wednesday]] 16:59:35
description::

Goal
- in class we analyzed poetry from the Tang Dynasty through close reading
- I want to analyze Tang poetry through distant reading
- My goal was to take a large collection of Tang poetry and find what characters showed up most frequently throughout the works.

Finding the poems
- I wanted to find a large collection of Tang poetry, in .txt form, containing the poets we discussed in class
- Found a collection called *Three Hundred Tang Poems*
- Project Gutenberg had a .txt version in Chinese and an audio version with an English table of contents.
	- https://www.gutenberg.org/ebooks/52323
	- https://www.gutenberg.org/ebooks/20968
- Using the English table of contents (and Google Translate), I found that this work contained some of the poets we discussed in class, such as Li Bai, Du Fu, and Wang Wei
- Isolated just the poetry and used that as the data set

Making the Wordclouds
- started by making a wordcloud
- https://github.com/amueller/word_cloud
- https://amueller.github.io/word_cloud/auto_examples/wordcloud_cn.html
- First wordcloud, no formatting, wanted to see what stuck out
	- Biggest strings of characters were author names
- Next wordcloud, separated each character so that the wordcloud would represent character frequency instead
- realized i cant make any sense of this so i need to print the most common characters

Translating to English and Refining the Data
- In order to analyze these characters I needed to translate them to English, so I used another script to give me the most frequent characters and how often they appear.
- I found that author names were one source of data contamination, and removed them from the .txt file
- Google Translate definitely was not able to translate some characters properly, but this list still conveys some of the common themes used in the 300 poems

Themes
- Nature, seen through words like Sun, Night, Sky, Wind, Cloud, Green, Autumn, Horse
	- A theme we first found prevalent in poetry from the Six Dynasties Period
	- Continues into this dynasty, such as in the nature descriptions Du Fu uses in poems like *A Song on How My Thatched Roof Was Ruined by the Autumn Wind*
	- Mountain is much higher than I thought it would be
- Passage of time, seen through words like Month, Year, Ancient, Today, Sun, Night, Autumn, Long, Time
- Dao/Way, mentioned 50 times
	- We've talked about Daoism in class, and it's interesting to see it show up so frequently in these poems
	- Is it being mentioned by multiple poets, or one or two poets that focused on Daoism?
		- After looking through the data, mentions of 道 are pretty spread out
		- Poems are organized by author for the most part, so no, it must be from multiple poets
- No mentions of wine/drinking
	- I thought we'd see more because of its frequent mention in Li Bai's poems


![[CHIN309_fig1.png]]![[CHIN309_fig2.png]]![[CHIN309_fig3.png]]

30 most common, before splitting into characters
```
[('作者：杜甫', 39), ('作者：李白', 34), ('作者：王維', 29), ('作者：李商隱', 24), ('作者：孟浩然', 15), ('作者：韋應物', 12), ('作者：劉長卿', 11), ('作者：杜牧', 10), ('作者：王昌齡', 8), ('作者：岑參', 7), ('作者：李頎', 7), ('作者：白居易', 6), ('作者：盧綸', 6), ('作者：張九齡', 5), ('作者：柳宗元', 5), ('作者：張祜', 5), ('作者：韓愈', 4), ('作者：劉禹錫', 4), ('作者：溫庭筠', 4), ('作者：崔顥', 4), ('作者：元稹', 4), ('雜詩', 3), ('作者：錢起', 3), ('作者：韓翃', 3), ('作者：李益', 3), ('作者：司空曙', 3), ('宮詞', 3), ('春思', 2), ('送別', 2), ('作者：常建', 2)]
```

30 most common characters
```
[('，', 1580), ('。', 1321), ('作', 351), ('者', 346), ('：', 322), ('不', 222), ('人', 214), ('山', 175), ('1', 172), ('0', 170), ('2', 163), ('？', 151), ('無', 134), ('一', 133), ('月', 130), ('日', 127), ('；', 123), ('夜', 120), ('天', 120), ('風', 117), ('白', 117), ('長', 112), ('來', 105), ('雲', 104), ('上', 102), ('有', 98), ('春', 95), ('江', 95), ('相', 94), ('何', 92)]
```

30 most common characters, ran through google translate
```
[(',', 1580), ('.', 1321), ('do', 351), ('who', 346), (':', 322), ('not', 222), ( 'person', 214), ('mountain', 175), ('1', 172), ('0', 170), ('2', 163), ('?', 151), ('none ', 134), ('one', 133), ('month', 130), ('day', 127), (';', 123), ('night', 120), ('day', 120), ('wind', 117), ('white', 117), ('long', 112), ('come', 105), ('cloud', 104), ('on', 102) , ('you', 98), ('spring', 95), ('jiang', 95), ('xiang', 94), ('he', 92)]
```

100 most common
```
[('，', 1580), ('。', 1321), ('作', 351), ('者', 346), ('：', 322), ('不', 222), ('人', 214), ('山', 175), ('1', 172), ('0', 170), ('2', 163), ('？', 151), ('無', 134), ('一', 133), ('月', 130), ('日', 127), ('；', 123), ('夜', 120), ('天', 120), ('風', 117), ('白', 117), ('長', 112), ('來', 105), ('雲', 104), ('上', 102), ('有', 98), ('春', 95), (7', 94), ('何', 92), ('行', 92), ('之', 91), ('生', 91), ('君', 90), ('李', 87), ('中', 87), ('水', 87), ('見', 85), ('花', 85), ('時', 84), ('王', 84), ('3', 83), ('下', 79), ('青', 79), ('歸', 78), ('如', 78), ('秋', 75), ('明', 72), ('萬', 72), ('三', 71), ('為', 71), ('落', 71), ('空', 70), ('自', 67), ('此', 64), ('金', 63), ('雨', 63), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9', 62), ('去', 62), ('今', 61), ('馬', 60), ('南', 59), ('杜', 59), ('城', 59), ('欲', 59), ('家', 58), ('將', 58), ('西', 58), ('古', 58), ('年', 58), ('未', 57), ('子', 57), ('門', 57), ('在', 56), ('心', 56), ('清', 56), ('飛', 56), ('寒', 56), ('聲', 56), ('客', 55), ('事', 54), ('處', 54), ('別', 54), ('朝', 54), ('高', 53), ('陽', 53), ('黃', 52), ('玉', 51), ('大', 51), ('入', 50), ('與', 50), ('出', 50), ('道', 50), ('望', 49), ('十', 49)]
```

100 most common characters, ran through google translate
```
[(',', 1580), ('.', 1321), ('do', 351), ('who', 346), (':', 322), ('no', 222), ( 'person', 214), ('mountain', 175), ('1', 172), ('0', 170), ('2', 163), ('?', 151), ('none ', 134), ('one', 133), ('month', 130), ('day', 127), (';', 123), ('night', 120), ('day', 120), ('wind', 117), ('white', 117), ('long', 112), ('come', 105), ('cloud', 104), ('on', 102) , ('you', 98), ('spring', 95), ('jiang', 95), ('xiang', 94), ('he', 92), ('line', 92), ( 'zhi', 91), ('sheng', 91), ('jun', 90), ('li', 87), ('zhong', 87), ('water', 87), ('see ', 85), ('flower', 85), ('time', 84), ('king', 84), ('3', 83), ('lower', 79), ('green', 79), ('Return', 78), ('Ru', 78), ('Autumn', 75), ('Ming', 72), ('Wan', 72), ('Three', 71) , ('wei', 71), ('fall', 71), ('empty', 70), ('si', 67), ('this', 64), ('jin', 63), ( 'rain', 63), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9 ', 62), ('go', 62), ('now', 61), ('ma', 60), ('nan', 59), ('du', 59), ('city', 59), ('desire', 59), ('home', 58), ('will', 58), ('west', 58), ('ancient', 58), ('year', 58) , ('wei', 57), ('zi', 57), ('door', 57), ('zai', 56), ('xin', 56), ('clear', 56), ( 'Fly', 56), ('Cold', 56), ('Sound', 56), ('Guest', 55), ('Thing', 54), ('Location', 54), ('Don't ', 54), ('towards' , 54), ('High', 53), ('Yang', 53), ('Yellow', 52), ('Jade', 51), ('Big', 51), ('In', 50 ), ('and', 50), ('out', 50), ('dao', 50), ('look', 49), ('ten', 49)]
```

Cleaning Up
```
,,. ,Do,Who,:,No,People,Mountain,1,0,2,? ,No, One, Month, Sun, ;, Night, Sky, Wind, White, Long, Come, Cloud, Up, Yes, Spring, River, Phase, He, Xing, Zhi, Sheng, Jun, Li, Zhong, Water , See, Flower, Time, King, 3, Down, Green, Return, Such as, Autumn, Ming, Ten Thousand, Three, For, Fall, Empty, Since, This, Gold, Rain, 4, 5, 6, 7, 8 ,9, Go, Today, Ma, South, Du, City, Desire, Home, Will, West, Ancient, Year, Wei, Zi, Door, In, Heart, Clear, Fly, Cold, Sound, Guest, Things, Place , Don't, Towards, High, Yang, Yellow, Jade, Big, In, With, Out, Dao, Look, Ten,
```

```
Do, People,Mountain,1,0,2,? ,No, One, Month, Sun, ;, Night, Sky, Wind, White, Long, Come, Cloud, Up, Yes, Spring, River, Phase, He, Xing, Zhi, Sheng, Jun, Li, Zhong, Water , See, Flower, Time, King, 3, Down, Green, Return, Such as, Autumn, Ming, Ten Thousand, Three, For, Fall, Empty, Since, This, Gold, Rain, 4, 5, 6, 7, 8 ,9, Go, Today, Ma, South, Du, City, Desire, Home, Will, West, Ancient, Year, Wei, Zi, Door, In, Heart, Clear, Fly, Cold, Sound, Guest, Things, Place , Don't, Towards, High, Yang, Yellow, Jade, Big, In, With, Out, Dao, Look, Ten,
```

```
do who no person mountain none one month day night day wind white long come cloud you spring jiang xiang he line zhi sheng jun li zhong water see flower time king lower green Return Ru Autumn Ming Wan Three wei fall empty si this jin rain go now ma nan du city desire home will west ancient year wei zi door zai xin clear Fly Cold Sound Guest Thing Location Dont towards High Yang Yellow Jade Big In and out dao look ten
```

```
('person', 214), ('mountain', 175), ('none ', 134), ('one', 133), ('month', 130), ('day', 127), ('night', 120), ('day', 120), ('wind', 117), ('white', 117), ('long', 112), ('cloud', 104), ('on', 102) , ('you', 98), ('spring', 95), ('jiang', 95), ('xiang', 94), ('he', 92), ('line', 92), ( 'zhi', 91), ('sheng', 91), ('jun', 90), ('li', 87), ('zhong', 87), ('water', 87), ('see ', 85), ('flower', 85), ('time', 84), ('king', 84), ('lower', 79), ('green', 79), ('Return', 78), ('Ru', 78), ('Autumn', 75), ('Ming', 72), ('Wan', 72), ('Three', 71) , ('wei', 71), ('fall', 71), ('empty', 70), ('si', 67), ('this', 64), ('jin', 63), ( 'rain', 63), ('go', 62), ('now', 61), ('ma', 60), ('nan', 59), ('du', 59), ('city', 59), ('desire', 59), ('home', 58), ('will', 58), ('west', 58), ('ancient', 58), ('year', 58) , ('wei', 57), ('zi', 57), ('door', 57), ('zai', 56), ('xin', 56), ('clear', 56), ( 'Fly', 56), ('Cold', 56), ('Sound', 56), ('Guest', 55), ('Thing', 54), ('Location', 54), ('Don't ', 54), ('towards' , 54), ('High', 53), ('Yang', 53), ('Yellow', 52), ('Jade', 51), ('Big', 51), ('In', 50 ), ('and', 50), ('out', 50), ('dao', 50), ('look', 49)
```

![[chart.png]]
![[Pasted image 20221022164946.png]]

Notable words
- Dao, 50
- Mountain, the most common noun after Person, beating out a lot of words like On, You, This that  I thought would be more common
- You is interesting, second person
- Water, Flower, Green, Autumn, Rain, Cold, 
- Fly, Desire
- Home, West, Guest, Location
- City, Jade
- Jiang 95, Xiang 94, Zhi 91 , Sheng 91, Jun 90, Li 87, Zhong 87, Ru 78, Ming 72, Wan 72, Wei 71, Si 67, Jin 63, Ma 60, Nan 59, Du 59, Wei 57, Zi 57, Zai 56, Xin 56, Yang 53, Dao 50
	- words that google couldnt translate
	- Names likely

```
this is the same thing from earlier just copy pasting to look at it

[(',', 1580), ('.', 1321), ('do', 351), ('who', 346), (':', 322), ('no', 222), ( 'person', 214), ('mountain', 175), ('1', 172), ('0', 170), ('2', 163), ('?', 151), ('none ', 134), ('one', 133), ('month', 130), ('day', 127), (';', 123), ('night', 120), ('day', 120), ('wind', 117), ('white', 117), ('long', 112), ('come', 105), ('cloud', 104), ('on', 102) , ('you', 98), ('spring', 95), ('jiang', 95), ('xiang', 94), ('he', 92), ('line', 92), ( 'zhi', 91), ('sheng', 91), ('jun', 90), ('li', 87), ('zhong', 87), ('water', 87), ('see ', 85), ('flower', 85), ('time', 84), ('king', 84), ('3', 83), ('lower', 79), ('green', 79), ('Return', 78), ('Ru', 78), ('Autumn', 75), ('Ming', 72), ('Wan', 72), ('Three', 71) , ('wei', 71), ('fall', 71), ('empty', 70), ('si', 67), ('this', 64), ('jin', 63), ( 'rain', 63), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9 ', 62), ('go', 62), ('now', 61), ('ma', 60), ('nan', 59), ('du', 59), ('city', 59), ('desire', 59), ('home', 58), ('will', 58), ('west', 58), ('ancient', 58), ('year', 58) , ('wei', 57), ('zi', 57), ('door', 57), ('zai', 56), ('xin', 56), ('clear', 56), ( 'Fly', 56), ('Cold', 56), ('Sound', 56), ('Guest', 55), ('Thing', 54), ('Location', 54), ('Don't ', 54), ('towards' , 54), ('High', 53), ('Yang', 53), ('Yellow', 52), ('Jade', 51), ('Big', 51), ('In', 50 ), ('and', 50), ('out', 50), ('dao', 50), ('look', 49), ('ten', 49)]
```

Is Google Translate a problem?
Definitely but it's the best option
Tried using periods between words to reduce characters being seen as together by translate

```
，. 。. 作. 者. ：. 不. 人. 山. 1. 0. 2. ？. 無. 一. 月. 日. ；. 夜. 天. 風. 白. 長. 來. 雲. 上. 有. 春. 江. 相. 何. 行. 之. 生. 君. 李. 中. 水. 見. 花. 時. 王. 3. 下. 青. 歸. 如. 秋. 明. 萬. 三. 為. 落. 空. 自. 此. 金. 雨. 4. 5. 6. 7. 8. 9. 去. 今. 馬. 南. 杜. 城. 欲. 家. 將. 西. 古. 年. 未. 子. 門. 在. 心. 清. 飛. 寒. 聲. 客. 事. 處. 別. 朝. 高. 陽. 黃. 玉. 大. 入. 與. 出. 道. 望. 十.

translates to

, . . . Do. Who. :. No. People. Mountains. 1. 0. 2. ? No. One. Month. Sun. ;. Night. Sky. Wind. White. Long. Come. Cloud. Up. See. Flower. Time. King. 3. Down. Green. Return. Such as. Autumn. Ming. Ten thousand. Three. 9. Go. Today. Horse. South. Du. City. Desire. Home. Will. West. Ancient. Year. Do not. Towards. High. Yang. Yellow. Jade. Great. In. and. Out. Dao.
```

The author lines are interfering
They arent being translated and when they are its wack
Removing author lines from the text file then running common words again

```
[('，', 1580), ('。', 1321), ('不', 222), ('人', 213), ('山', 175), ('1', 172), ('0', 170), ('2', 163), ('？', 151), ('一', 133), ('無', 133), ('月', 130), ('日', 127), ('；', 123), ('夜', 120), ('天', 120), ('風', 117), ('來', 105), ('雲', 104), ('上', 102), ('長', 101), ('有', 98), ('江', 95), ('春', 94), ('相', 94), ('何', 92), ('行', 92), ('生', 91), ('君', 90), ('之', 88), ('水', 87), ('中', 86), ('見', 85), ('花', 85), ('時', 84), ('3', 83), ('下', 79), ('青', 79), ('歸', 78), ('如', 78), ('白', 77), ('秋', 74), ('明', 72), ('萬', 72), ('三', 71), ('落', 71), ('為', 70), ('自', 67), ('空', 67), ('此', 64), ('雨', 63), ('金', 62), ('4', 62), ('5', 62), ('6', 62), ('7', 62), ('8', 62), ('9', 62), ('去', 62), ('今', 61), ('南', 59), ('城', 59), ('欲', 59), ('家', 58), ('將', 58), ('馬', 58), ('古', 58), ('年', 58), ('未', 57), ('門', 57), ('西', 57), ('在', 56), ('心', 56), ('清', 56), ('飛', 56), ('寒', 56), ('子', 56), ('聲', 56), ('客', 55), ('事', 54), ('處', 54), ('別', 54), ('朝', 54), ('陽', 53), ('黃', 52), ('高', 51), ('大', 51), ('入', 50), ('與', 50), ('玉', 50), ('出', 50), ('道', 50), ('望', 49), ('十', 49), ('流', 49), ('二', 48), ('歌', 48), ('送', 48), ('宮', 48), ('得', 47)]

just the characters

，. 。. 不. 人. 山. 1. 0. 2. ？. 一. 無. 月. 日. ；. 夜. 天. 風. 來. 雲. 上. 長. 有. 江. 春. 相. 何. 行. 生. 君. 之. 水. 中. 見. 花. 時. 3. 下. 青. 歸. 如. 白. 秋. 明. 萬. 三. 落. 為. 自. 空. 此. 雨. 金. 4. 5. 6. 7. 8. 9. 去. 今. 南. 城. 欲. 家. 將. 馬. 古. 年. 未. 門. 西. 在. 心. 清. 飛. 寒. 子. 聲. 客. 事. 處. 別. 朝. 陽. 黃. 高. 大. 入. 與. 玉. 出. 道. 望. 十. 流. 二. 歌. 送. 宮. 得.

translates to

, . . . No. People. Mountains. 1. 0. 2. ? One. No. Month. Sun. ;. Night. Sky. Wind. Comes. Cloud. Up. Long. Time. 3. Down. Green. Return. Such as. White. Autumn. Ming. Wan. Three. Fall. Today. South. City. Desire. Home. Will. Horse. Ancient. Year. . Yellow. Tall. Big. In. And. Jade. Out. Dao.

but thats not all, there should be more words after Dao, Google Translate just won't cooperate
by copy pasting only some characters at a time, I was able to get these words to appear:

，. 。. 不. 人. 山. 1. 0. 2. ？. 一. 
, . . . No. People. Mountains. 1. 0. 2. ? . One.

無. 月. 日. ；. 夜. 天. 風. 來. 雲. 上. 長. 有. 江.
No. Month. Sun. ;. Night. Sky. Wind. Comes. Cloud. Up. Long. There is. River.

春. 相. 何. 行. 生. 君. 之. 水. 中. 見. 
Spring. Phase. What. Travel. Life. Jun. Of. Water. Middle. See.

花. 時. 3. 下. 青. 歸. 如. 白. 秋. 明. 萬. 三. 
Flower. Time. 3. Down. Green. Returning. Such as. White. Autumn. Ming. Wan. Three.

落. 為. 自. 空. 此. 雨. 金. 4. 5. 6. 
Fall. For. From. Empty. This. Rain. Gold. 4. 5. 6.

7. 8. 9. 去. 今. 南. 城. 欲. 家. 將. 馬. 古. 年.  
7. 8. 9. Go. Today. South. City. Desire. Home. Will. Horse. Ancient. Year.

未. 門. 西. 在. 心. 清. 飛. 寒. 子. 聲. 客. 事.
Not. Door. West. In. Heart. Clear. Flying. Cold. Son. Sound. Guest. Things.

處. 別. 朝. 陽. 黃. 高. 大. 入. 與. 玉.
Where. Don't. Facing. Yang. Yellow. High. Big. Entering. And. Jade.

出. 道. 望. 十. 流. 二. 歌. 送. 宮. 得.
Out. Dao. Hope. Ten. Stream. Two. Song. Send. Palace. Get.

```

```
leaves us with this final translated list, excluding symbols, and excluding arabic numberals

No. People. Mountains. One. No. Month. Sun. Night. Sky. Wind. Comes. Cloud. Up. Long. There is. River. Spring. Phase. What. Travel. Life. Jun. Of. Water. Middle. See. Flower. Time. Down. Green. Returning. Such as. White. Autumn. Ming. Wan. Three. Fall. For. From. Empty. This. Rain. Gold. Go. Today. South. City. Desire. Home. Will. Horse. Ancient. Year. Not. Door. West. In. Heart. Clear. Flying. Cold. Son. Sound. Guest. Things. Where. Don't. Facing. Yang. Yellow. High. Big. Entering. And. Jade. Out. Dao. Hope. Ten. Stream. Two. Song. Send. Palace. Get.
```

Notes
- Mountains
	- way higher than other more common words
- Month Year Ancient
- Sun Night Sky Wing Cloud Green Autumn Horse
- Today
- Return Desire South City Home
- Jade
- Dao

![[Pasted image 20221022191816.png]]
![[Pasted image 20221022192453.png]]
how do i disable the vertical characters 💀