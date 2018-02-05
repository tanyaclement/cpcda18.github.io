##Week 10
###Objectives
- Sentence tokenization
- General Text Statistics
- Exploratory data analysis
- Visualizing general statistics
<!--
Look at Python cookbook chapter 6 in week 8 files on Canvas.
-->
### Exercises
Right click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 3: Text Analysis](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/answerbook/Chapter%203%20-%20Text%20analysis.ipynb)

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

<!--

Topics to Cover
---------------

-   preprocessing for text machine learning:

    -   removing stop words

    -   lemmatizing

-   classifying texts using scikit-learn

-   author attribution

-   cluster analysis



Provide collection of several hundred texts grouped by genre:

- news articles
- blog posts
- literary prose
- poetry
- scientific articles
- spam emails

Have students choose two or three categories to work with.

Using scikit-learn rain ML model using small number of texts and measure classification accuracy for remaining set.

Train model using more texts and see if there’s any improvement.

Compare models.

Look at mis-classified texts and discuss what features make them outliers.



#### Break

Demonstrate cluster analysis.


Sentiment analysis: Evaluate/classify Twitter data.
-->
