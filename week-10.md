## Week 10
### Objectives
- Unsupervised learning: Latent Dirichlet allocation (LDA) topic modeling
- Supervised learning: Naive Bayes classification
- Fetching and Parsing Data from the Web with OpenRefine, Advanced APIs

### Exercises
Select `Raw` at the following link and save the Jupyter notebook files to `sharedfolder` on your desktop.

Save the Jupyter notebook file to `sharedfolder` on your desktop.

1. [Week-10_Machine-Learning](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-10_Machine-Learning.ipynb)

2. [Karsdorp, Chapter 3: Text Processing](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/old/Appendix%20-%20Text%20Preprocessing.ipynb)
- You'll want to be sure that you have completed [Chapter 2: The Basics](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/answerbook/Chapter%202%20-%20The%20basics.ipynb) before tackling these exercises. Chapter 2 is also a great reference if you need a reminder of what different functions do.

3. [Karsdorp, Chapter 3: Text Analysis](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/answerbook/Chapter%203%20-%20Text%20analysis.ipynb)

4. [Fetching and Parsing Data from the Web with OpenRefine, Advanced APIs](https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine) *Example 3: Advanced APIs*

- Using OpenRefine: Start the application on the lab computer on the Mac side. It only works through a
browser window. If the browser window doesn’t open automagically after doubleclicking on the application, copy and paste http://127.0.0.1:3333/ into your browser window.
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
