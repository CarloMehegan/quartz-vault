Tags: #flashcards #assignment #CSCI100
Created: Wednesday, Apr 13

# Final Project Outline

### Research Question
How does current music taste differ among Russia's neighboring countries?

### I. Getting the Data
Briefly describe your data, the format it is in, and list your data sources. For example, you may be obtaining data from websites – list the specific websites and describe whether you are able to download text files, you are creating text files, you are using OCR, etc. Will you need to collect your data via a survey? How will you do that?

We are using Spotify's Top 50 playlists; these show the most popular songs in a country (ranked by Spotify's algorithm). We use Spotify data because the platform collects a lot of metadata - for each song, they collect basic information like the artist and the genre, but also more specific data that helps their algorithm find related songs. This specific data includes information like subgenres, tempo, key, time signature, decibel volume, and even ratings for more abstract concepts, like how 'happy' or 'danceable' a song is.

To extract this data from Spotify, we are using Chosic's playlist analyzer. This website is meant to help Spotify users make better playlists, but we can also use it to convert playlists into CSV files containing each song and its metadata.

We are collecting CSV files for 11 different Spotify playlists, and since these playlists are automatically updated every day, we plan to collect data at least five times a week in order to analyze not only how the data changes between countries, but also how each country changes over time

### II. Data Pre-processing
What pre-processing will you have to do of your data? Will you need to convert your data to another format (e.g. from pdf to text, or from html to text)? For text data, will you be removing punctuation and/or stopwords? Will you have a custom set of stopwords? Will you be removing any data prior to your analysis? Will you be searching for specific terms?

Chosic does a good job of formatting the CSV files, so we don't need to do anything to the contents of each file. However, because we are collecting many files of data, we want to name each file in a way that makes it easy to go through all of them in code. We have decided to use the format "041022 Ukraine"; the date of which the data was collected, and the country it is from. We can easily process files from a specific date or specific country this way. Because we are using titles, authors, genres, etc., we do not need to take stopwords into account.

### III. Data Analysis
Describe the data analysis you will do. Be specific as to computational tools you will use – it is not enough just to say Python. This is the place to figure out if you need to learn about/access additional tools. If you don’t know what tool you need, describe the type of analysis you need to do and we will help you to find the tool.

In order to extract data from the csv files, we are using the pandas python library. Then, we can use the nltk and wordclouds libraries in order to create graphics and analyze the data we receive. As of right now, our analysis is exploratory. Once we collect an ample amount of data, we will look at what trends emerge and figure out ways to analyze them.


### IV. Presentation of Results and Conclusions
Ultimately you will need to prepare slides for a presentation. What will be on those slides? What sorts of visualizations will you need to display your results? Make sure your visualizations are appropriate for the kind of data you will present. Will you prepare a web page or a handout in addition to your presentation?

For our slides, the team plans to demonstrate the progression of the Top 50 playlists over the last few weeks. We will have slides to break down consecutive days, noting and visualizing the major changes in the rankings, as well as comparing and contrasting the countries we collect data for. We will use word clouds, frequency distributions, and other graphs in order to show our findings visually. We can analyze genre frequency, artist frequency, changes over time, geographic differences, and more. In our website, our data will be presented and organized among different tabs, so that viewers may navigate our findings.