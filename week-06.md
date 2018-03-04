## Week 6

### Objectives
Wget and Applied Archival Downloading

### Exercises
1. ["Applied Archival Downloading with Wget"](https://programminghistorian.org/lessons/applied-archival-downloading-with-wget) lesson in Programming Historian by Kellen Kurschinski.
*some hints!*
- Since we are using our Jupyter Notebook thru our Docker Container, you'll have tweak the assignment a little bit by doing some code editing and some environment switching: so, (1) build the python script in your text editor (Atom, for example), (2) save it in your /sharedfolder (be sure it ends in .py), (3) execute the python file through the command line to produce your "url.txt" file and (4) load that "url.txt" file into the Jupyter Notebook using the code provided in the lesson (your Jupyter Notebook is already situated in the sharedfolder so you don't have to navigate to that directory.)
- Reference the [Wget Manual](https://www.gnu.org/software/wget/manual/wget.html) if you are curious about the code bits.
- And, if you're really stuck, [check out the workaround](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Week_06_ProgrammingHistorian_workaround.ipynb).
- There is also one thing that has changed since this tutorial was written:  
This:
"http://chroniclingamerica.loc.gov/search/pages/results/?state=" + value.escape('url') + "&date1=" + cells['year'].value.escape('url') + "&date2=" + cells['year'].value.escape('url') + "&dateFilterType=yearRange&sequence=1&sort=date&rows=5&format=json"
has to be (*notice the https change*):
"*https*://chroniclingamerica.loc.gov/search/pages/results/?state=" + value.escape('url') + "&date1=" + cells['year'].value.escape('url') + "&date2=" + cells['year'].value.escape('url') + "&dateFilterType=yearRange&sequence=1&sort=date&rows=5&format=json"
- Finally, it *is not advised* unless you have expertise in downloading and installing packages, but if you want to do this on your machine without using Docker, there are handy instructions in the [Automated Downloading with Wget](https://programminghistorian.org/lessons/automated-downloading-with-wget) on Programming Historian by Ian Milligan

2. ["Fetching and Parsing Data from the Web with OpenRefine"](https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine) *Example 1: Fetching and Parsing HTML and Example 2: URL Queries and Parsing JSON* in Programming Historian by Evan Peter Williamson

*hints* refer to [Week 4](https://tanyaclement.github.io/cpcda18.github.io/week-04.html) if you are having trouble opening OpenRefine.

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
