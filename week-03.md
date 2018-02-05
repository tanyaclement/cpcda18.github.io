## Week 3

### Objectives

#### Lists
* list
* mutable versus immutable
* .split()
* .append()
* nested lists
* .remove()
* .sort()

#### Dictionaries
* dictionary
* indexing or accessing keys of dictionaries
* adding items to a dictionary
* .keys()
* .values()

### Exercises
You should already have this notebook in your shared folder from last week, but if not, click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 1:](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/Chapter%201%20-%20Getting%20started.ipynb)
Work through "Dictionaries"

### Getting started
In macOS, open Terminal and enter the following commands to launch the Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container
```

In Windows 10, open PowerShell and enter the following commands to launch the Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume C:\Users\***username_here***\Desktop\sharedfolder:/sharedfolder/ pcda17/ubuntu-container
```

Open any browser and type (your Juypter Notebook will launch):
```
localhost:8889

```
