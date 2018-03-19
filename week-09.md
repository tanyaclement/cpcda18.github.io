## Week 9

### Objectives
- Sentence tokenization
- Sentence Splitting
- Simple Tokenization
- Extracting n-grams
- Computing a Frequency Distribution
- Finding files and reading a corpus
- General Text Statistics
- Exploratory data analysis
- Visualizing general statistics

### Exercises
Save the following Jupyter notebook files to `sharedfolder` on your desktop.

1. [Using the Google Books REST API](https://github.com/tanyaclement/cpcda18.github.io/blob/master/week-09.1_Google_Books_API.ipynb)

2. [New York Times article scrape](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-09.2_NYT_Article_Scrape.ipynb)

3. Save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 3: Text Processing](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/old/Appendix%20-%20Text%20Preprocessing.ipynb)
- You'll want to be sure that you have completed [Chapter 2: The Basics](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/answerbook/Chapter%202%20-%20The%20basics.ipynb) before tackling these exercises. Chapter 2 is also a great reference if you need a reminder of what different functions do.

<!--
Look at Python cookbook chapter 6 in week 8 files on Canvas.
-->
### Getting started
Open Terminal in macOS and launch our Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container
```

In Windows 10, open PowerShell and enter the following to launch the Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume C:\Users\***username_here***\Desktop\sharedfolder:/sharedfolder/ pcda17/ubuntu-container
```

Open any browser and type (your Juypter Notebook will launch):
```
localhost:8889
```
