## Week 9

### Objectives
- Using the Google Books REST API
- New York Times article scrape
- Scraping and Parsing XML
- Fetching and Parsing Data from the Web with OpenRefine, APIs

### Exercises
Save the following Jupyter notebook files to `sharedfolder` on your desktop.

1. [Using the Google Books REST API](https://github.com/tanyaclement/cpcda18.github.io/blob/master/week-09.1_Google_Books_API.ipynb)

2. [New York Times article scrape](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-09.2_NYT_Article_Scrape.ipynb)

3. [Scraping and Parsing XML](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week-09.3_Scraping-and-Parsing-XML.ipynb)

4. [Fetching and Parsing Data from the Web with OpenRefine, APIs](https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine) *Example 2: URL Queries and Parsing JSON*

- Using OpenRefine: Start the application on the lab computer on the Mac side. It only works through a
browser window. If the browser window doesn’t open automagically after doubleclicking on the application, copy and paste http://127.0.0.1:3333/ into your browser window.

<!--
Look at Python cookbook chapter 6 in week 8 files on Canvas.
-->
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
