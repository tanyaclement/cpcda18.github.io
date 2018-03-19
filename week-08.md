## Week 8
### Objectives
- CSV Input/Output in Python
- Using the Google Books REST API
<!-- Look at Python cookbook chapter 6 in week 8 files on Canvas.-->

### Exercises
1. Download these Notebooks into your `/sharedfolder` directory:
- [week-08.1_CSV-Input-Output](https://github.com/tanyaclement/cpcda18.github.io/blob/master/week-08.1_CSV-Input-Output.ipynb)
- [Week_08.2_CSV_InputOutput_Python_MOMA](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week_08.2_CSV_InputOutput_Python_MOMA.ipynb)


<!--
```python3
outpath = "/sharedfolder/art_1960s.csv"
o = open(outpath, 'w')
a = csv.writer(o)
a.writerow(artwork_header)
a.writerows(art_1960s_sorted)
o.close()
```
-->


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
Look at Python cookbook chapter 6 in week 8 files on Canvas.

Click `Create Project`, then `Choose Files` and choose `V_and_A_ivory.csv`. Click `Next`. In the following window, click `Create Project` in the upper right corner.

At the top of the “place” column, click the dropdown button and choose “Text Facet.” A list of places will appear in the left column. Click “Paris” to display only works created there.

Note that several “place” records are listed as “Germany,” while others are German cities. Let’s group them under a single facet.
-->

<!--

- [Data Visualization and Statistics](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/week-8_Stats-and-Visualization.ipynb)


Navigate to [localhost:8889](localhost:8889) in your browser to open the notebook.


### Resources


- [Matplotlib gallery](https://matplotlib.org/gallery.html)

- [Matplotlib tutorial](http://www.labri.fr/perso/nrougier/teaching/matplotlib/)

- [Numpy quickstart tutorial](https://docs.scipy.org/doc/numpy-dev/user/quickstart.html)

- [scipy.stats tutorial](https://docs.scipy.org/doc/scipy/reference/tutorial/stats.html)

- [An introduction to Numpy and SciPy](https://engineering.ucsb.edu/~shell/che210d/numpy.pdf)


## Topics to Cover

- Descriptive statistics using numpy Python module
- Creating graphs in the matplotlib Python module

- Visualization

    - Tutorial source: [http://www.labri.fr/perso/nrougier/teaching/matplotlib/](http://www.labri.fr/perso/nrougier/teaching/matplotlib/)


Tutorial source for statistical tests on literary works:

- http://digitalhumanities.org/companion/view?docId=blackwell/9781405103213/9781405103213.xml&doc.view=print&chunk.id=ss1-4-4&toc.depth=1&toc.id=0

-->
