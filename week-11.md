## Week 11
### Objectives
- Supervised learning with multiple classifiers: Naive Bayes, k-nearest neighbor, Logistic Regression, Support Vector Machine (SVM), Multi-layer perceptron classifier
### Exercises
Select `Raw` at the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
1. [Unsupervised Learning: k-means clustering](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-11.1_Clustering.ipynb)
2. [Supervised Learning](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-11.2_Supervised-learning.ipynb)


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
