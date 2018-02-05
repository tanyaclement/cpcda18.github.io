## Week 5

### Objectives
* Putting together conditionals and loops in functions
- Reading files
- Writing a function
- Text clean up
- Writing results to a file

### Exercises
Right click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 2: First Steps](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/Chapter%202%20-%20First%20steps.ipynb)

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

<!--

[https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/week-05.ipynb](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/week-05.ipynb)


Go to [localhost:8889](localhost:8889) and click on `week-05.ipynb` to launch the notebook.

-->
