## Week 4
##Objectives
#### Conditions
* conditions
* indentation
* if
* elif
* else
* True
* False
* empty objects are false
* not
* in
* and
* or
* multiple conditions

#### Loops
* loop
* for statement
* iterable objects
* variable assignment in a for loop

#### Introducing OpenRefine

### Exercises
- Right click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 1:](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/Chapter%201%20-%20Getting%20started.ipynb)

- OpenRefine is very easy to download and run from your computer. You can get the download here: [http://openrefine.org/](http://openrefine.org/).

*Note: Today's OpenRefine tutorial is in a zip file in this week's files on Canvas.* If you would like to run OpenRefine from Docker, see below.

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

### Getting started running OpenRefine from Docker

Open a new terminal window and run the following command to download and run a Dockerized copy of the tabular data cleaning program OpenRefine.

```
docker run --name openrefine -d -p 3334:3333 psychemedia/docker-openrefine
```

If you get an error that says you already have a container with this name (because you're coming back to using OpenRefine from Docker, perhaps) close and remove all current Docker containers, enter the following command:

```
docker rm $(docker ps -aq)
```

Enter the following address in your browser’s URL bar to open the application.

- [http://127.0.0.1:3334/](http://127.0.0.1:3334/)
