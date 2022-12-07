# renaming a folder of files
```python
#get today's date, and format it

from datetime import date

today = date.today()

formatteddate = today.strftime("%m%d%y")

  

#replace the "Top 50 - " in the file name, leaving just "041022 Russia" for example

import os

for fileName in os.listdir("."):

 os.rename(fileName, fileName.replace("Top 50 - ", formatteddate + " "))
 ```
 code used for [[CS100 Final Project]]
 