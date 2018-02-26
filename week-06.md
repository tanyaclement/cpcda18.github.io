## Week 6

### Objectives
Wget and Applied Archival Downloading

### Exercises
 - ["Applied Archival Downloading with Wget"](https://programminghistorian.org/lessons/applied-archival-downloading-with-wget) lesson in Programming Historian by Kellen Kurschinski.

*some hints!*
1. If you want to do this on your machine without using Docker, there are handy instructions in the [Automated Downloading with Wget](https://programminghistorian.org/lessons/automated-downloading-with-wget) on Programming Historian by Ian Milligan
2. If you are going to use your Jupyter Notebook thru our Docker Container, you'll have to do some code editing and some environment switching: build the python script in your text editor (Atom, for example), save it in your /sharedfolder (be sure it ends in .py), and then execute that file through Jupyter Notebook using the code provided in the lesson (your Jupyter Notebook is already situated in the sharedfolder so you don't have to navigate to that directory.)
3. Reference the [Wget Manual](https://www.gnu.org/software/wget/manual/wget.html) if you are curious about the code bits.

 - *Example 1: Fetching and Parsing HTML and Example 2: URL Queries and Parsing JSON* ["Fetching and Parsing Data from the Web with OpenRefine"] (https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine) lesson in Programming Historian by Evan Peter Williamson

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
