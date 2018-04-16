## Week 12
### Objectives

- Matplotlib
  - Simple Viz for Sentiment Analysis
  - Much more Viz
- Tableau

### Exercises
- Matplotlib: Select `Raw` at the following link and save the Jupyter notebook files to `sharedfolder` on your desktop.
  - [Simple Viz for Sentiment Analysis](https://github.com/tanyaclement/cpcda18.github.io/blob/master/week-12.1_Stats-and-Visualization.ipynb)
  - [Much more Viz](https://github.com/tanyaclement/cpcda18.github.io/blob/master/week-12.2_Matplotlib_Visualization_Examples.ipynb)
- Tableau
-- [free download for students](https://www.tableau.com/academic/students)
-- [tutorial](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/get-started-tutorial-home.html)

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

Download a Jupyter notebook from the list below to `sharedfolder` on your desktop.


Navigate to [localhost:8889](localhost:8889) in your browser to open the notebook.


### Other Resources

- [Data Visualization LibGuide](https://guides.lib.utexas.edu/data-visualization/resources)
