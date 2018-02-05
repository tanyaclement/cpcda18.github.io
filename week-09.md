## Week 9:
###Objectives
<!--
Look at Python cookbook chapter 6 in week 8 files on Canvas.
-->
- Introducing OpenRefine

### Exercises

OpenRefine is very easy to download and run from your computer. You can get the download here: [http://openrefine.org/](http://openrefine.org/).

*Note: Today's OpenRefine tutorial is in this week's files on Canvas.* If you would like to run OpenRefine from Docker, see below.

### Getting started running OpenRefine from Docker

Open a new terminal window and run the following command to download and run a Dockerized copy of the tabular data cleaning program OpenRefine.

```
docker run --name openrefine -d -p 3334:3333 psychemedia/docker-openrefine
```

Enter the following address in your browser’s URL bar to open the application.

- [http://127.0.0.1:3334/](http://127.0.0.1:3334/)
<!--
Right click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.


- [Machine Learning 1](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/Week-09_Machine-Learning.ipynb)


Navigate to [localhost:8889](localhost:8889) in your browser to open the notebook.
-->
