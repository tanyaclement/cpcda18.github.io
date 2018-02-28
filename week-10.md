## Week 10
### Objectives
- Unsupervised learning: Latent Dirichlet allocation (LDA) topic modeling
- Supervised learning: Naive Bayes classification

### Exercises
- Select `Raw` at the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.

[https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-10_Machine-Learning.ipynb](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-10_Machine-Learning.ipynb)

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
