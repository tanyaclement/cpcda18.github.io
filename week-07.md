##Week 7
###Objectives
- Type casting
- String Manipulation
* split()
* join()
* find()
* replace()
* strip() and newlines
* lower() and upper() - Changing Case

- Iterables, Iteration & Loops¶
* Tuples & Sets
* enumerate()
* zip()
* sorted() and reverse()
* min(), max() and sum()

- List comprehensions
- Importing external modules
- While loop
- File Input/Output
- Functions

<!--
explain Rest APIs by showing how a google search can change by changing the URL
-->
### Exercises
- Select `Raw` at the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 2: The Basics](https://github.com/tanyaclement/cpcda18.github.io/blob/master/Chapter%202%20-%20The%20basics.ipynb)

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
<!--
Sample datasets from The Museum of Modern Art (MoMA) [via GitHub](https://github.com/MuseumofModernArt/collection). Download these files to your /sharedfolder/ on your desktop.
- [Artists.csv](https://media.githubusercontent.com/media/MuseumofModernArt/collection/master/Artists.csv)
- [Artworks.csv](https://media.githubusercontent.com/media/MuseumofModernArt/collection/master/Artworks.csv)

-->
<!--

#### CSV I/O in Python
Paste the following code snippet into a new Jupyter notebook.

```python3
import csv

artist_csv_path = "/sharedfolder/Artists.csv"
artist_table = []

with open(artist_csv_path) as fi:
    csv_input = csv.reader(fi)
    for row in csv_input:
        artist_table.append(row)

artist_header = artist_table[0]
artist_table.remove(artist_table[0])

artist_header
```

![](week/3/Image-0.png)

Check the length of the table, then enter an index value in brackets to look at an entry.

```python3
print(len(artist_table))

artist_table[6310]
```

We’ve just copied all the data from a CSV-formatted spreadsheet and turned it into a format Python can easily work with: a list of lists of strings. Let’s walk through the above a step at a time, this time loading MoMA’s artwork metadata.

We began by importing the `csv` module, Python’s built-in CSV input/output tool. Note, since you've already done it above, you don't have to do it again.

```python3
import csv
```
Next we assign our pathname to the `artwork_path` variable and initialize an empty list called `artwork_table`. This will become our list of lists, Python’s version of a table. Add the below to your open notebook.

```python3
artwork_csv_path = "/sharedfolder/Artworks.csv"
artwork_table = []
```

Then we create a file stream object `fi` that points to our spreadsheet, We pass our file object to `csv`’s constructor function and assign the new reader object to `csv_file`. Finally, using a for loop, we iterate through our csv object and add each row (represented by a list) to the master list `artwork_table`.

```python3
with open(artwork_csv_path) as fi:
    csv_file = csv.reader(fi)
    for row in csv_file:
        artwork_table.append(row)
```

Because this table uses column labels in the first row, we’ll save those labels to the variable `header` and remove it from the table.

```python3
artwork_header = artwork_table[0]
artwork_table.remove(artwork_table[0])
```

Finally, let’s look at our list of column titles …

```python3
artwork_header
```

… as well as a row in our table.

```python3
artwork_table[60946]
```

 **Tip:** Python will ignore any text following the “#” character on a line, which we can use to add explanatory comments within our code. Here are a couple lines from the snippet above followed by example notes.

>     artwork_header = artwork_table[0]  # saves list of column titles to variable 'artwork_header'
>     artwork_table.remove(artwork_table[0])  # removes header row


#### Quick Assignment
Write a piece of code that prints each column label in `artist_header` and `artwork_header` next to its index in the list, beginning from zero as usual. You may want to keep this reference handy for the next few exercises.

 _A possible solution:_

```python3
print('Artists\n')

for i in range(len(artist_header)):
    print(str(i) + ' ' + artist_header[i])

print('\nArtworks\n')

for i in range(len(artwork_header)):
    print(str(i) + ' ' + artwork_header[i])
```
#### Quick Assignment
Write a piece of code that creates a new table (i.e., list of lists) containing only artists born in the 1880s.

 _A possible solution:_

```python3
born_1880s = []

for row in artist_table:
    if 1880 <= int(row[5]) <= 1889:
        born_1880s.append(row)
```

#### Average Artist Age
Now that we’ve defined a meaningful subset of our data, let’s see what we can do with it. For instance, what was the mean life span of artists born in the 1880s (who happen to be included in MoMA's collections)?

```python3
lifespans_1880s = []

for row in born_1880s:
    lifespans_1880s.append(int(row[6]) - int(row[5]))

lifespans_1880s
```   
![](week/3/Image-1.png)

If you scroll through your list of lifespans, you’ll see occasional negative numbers (e.g., “-1887”). Since missing values are represented by “0,” if no death date is listed we’ll end up subtracting an artist’s birth year from zero. Let’s amend our code to leave out these rows.

```python3
lifespans_1880s = []

for row in born_1880s:
    age = int(row[6])-int(row[5])
    if age > 0:
        lifespans_1880s.append(age)

lifespans_1880s
```
Now that we have a list of valid integers, all we need to do is calculate the mean. Below we divide the sum of the list (which we cast as a float) by its length to get 72.65 years.

```python3
float(sum(lifespans_1880s)) / len(lifespans_1880s)
```

That format is a bit verbose for a simple task like this, so to make life easier we’ll use the Python package `NumPy`.

```python3
import numpy
numpy.mean(lifespans_1880s)
```
**Tip:** The code above imports the entire `numpy` package. Python also lets us import packages’ individual functions to the current environment, which can make code more compact.

```python3
from numpy import mean
mean(lifespans_1880s)
```
A common convention is to rename `numpy` to `np` at the import step.

```python3
import numpy as np
np.mean(lifespans_1880s)
```

This guide will use to `numpy.mean()` for the sake of clarity, but feel free to set up your environment however you like.

#### Quick Assignment
Write a piece of code that creates a new table containing all artworks that include the term “Fluxus” in any metadata field.

 _A possible solution:_

```python3
fluxus_table = []

for row in artwork_table:
    for cell in row:
        if 'fluxus' in cell.lower():
            if row not in fluxus_table:
                fluxus_table.append(row)
```

#### Fluxus Metadata Continued
Now let’s make a master list of entries under “medium” in our Fluxus metadata set.

```python3
medium_list = []

for row in fluxus_table:
    medium_list.append(row[9])

len(medium_list)
```

Let’s look at 10 random samples from the collection, first importing the `random` package.

```python3
import random

random.sample(medium_list, 10)
```

![](week/3/Image-2.png)

Let’s see what terms appear most frequently in our list of media.

```python3
from collections import Counter

c = Counter(medium_list)
c.most_common(10)
```

![](week/3/Image-3.png)
Note that 1151 artworks are missing an entry for “medium,” with the term “(CONFIRM)” appearing 190 times.

#### Quick Assignment
Returning to our original MoMA metadata table, write a piece of code that extracts only works created in the 1960s (or another decade of your choosing). Since the date field in MoMA’s metadata doesn’t follow a strictly defined numerical format, you’ll have to think about how to interpret values like “1963,” “1963-5“, “c. 1963,” “c. 1960s,” etc.

Let students struggle with this a bit, then encourage them to settle on a relatively quick and dirty solution. The collection doesn’t have to be perfect; we’ll be cleaning the table in OpenRefine later.

 _A simple solution with high recall and low precision:_

```python3
art_1960s = []

for row in artwork_table:
    if '196' in row[8]:
        art_1960s.append(row)
```

<!--
 _A way-too-elaborate solution with better precision but imperfect recall:_

```python3
import string

def date_span(date_string):
         if len(date_string) == 0:return[-1,-1]
         temp_string = date_string
         if ', 1' in temp_string:
             temp_string = date_string.split(',')[1]
         elif ',' in temp_string:
             temp_string = date_string.split(',')[0]
         temp_string = temp_string.lower().replace('early ','').replace('late ','')
         if (len(temp_string)0)&(temp_string[0] != ['(']):
             temp_string = temp_string.split('(')[0]
         temp_string = temp_string.translate(None,"(){}<[]; ")
         try:
             if 'c.' in temp_string:
                 temp_string = temp_string.replace('c.','').strip()
             if temp_string.isdigit():
                 return [int(temp_string),int(temp_string)]
             if temp_string[-2:] == '0s':
                 return [int(temp_string.strip('s')),int(temp_string.strip('s'))+9]
             if '-' in temp_string:
                 pair = temp_string.split('-')
                 if len(pair[1].strip()) == 2:
                     return [int(pair[0].strip()),int(pair[0][:2]+pair[1].strip())]
                 elif len(pair[1]) == 4:
                     return [int(pair[0].strip()),int(pair[1].strip())]

                 else: print "error1: "+date_string + "- " + temp_string
         except: print "error2: "+date_string + " - " + temp_string

     art_temp = []
     for row in artwork_table:
         if '196' in row[8]:
             art_temp.append(row)

     art_1960s = []
     for row in art_temp:
         years = date_span(row[8])
         art_1960s.append(row)


    at_1960s[:15]
```

Note that the code above is an example of a decision tree, the absolute simplest kind of “artificial intelligence” algorithm.


#### Sorting a Table by Column

We can sort a table based on the values in a given column with the `sorted` function and and the `itemgetter` tool, which we use to specify the column we’re sorting by. The following sorts the table `art_1960s` by artist name (i.e., index `1` in each row).

```python3
from operator import itemgetter
art_1960s_sorted = sorted(art_1960s, key = itemgetter(1))
```

Since each row is so long, let’s just look at our sorted set of authors. The following notation returns a list of  each row’s “Artist” cell, located at index `1`.

```python3
[row[1] for row in art_1960s_sorted]
```

![](week/3/Image-4.png)

Let's look at the most common nationalities in our table of 1960s artworks. Here we’re once again using the `Counter` constructor from the `collections` package.

```python3
c = Counter([row[4] for row in art_1960s_sorted])
c.most_common(20)
```
![](week/3/Image-5.png)

It’s impossible to memorize the details of every specialized tool available in Python, so you’ll probably end up repeatedly looking up processes like these.

#### Writing CSVs
Now that we’ve filtered and sorted our metadata, let’s export it to a new CSV file called `art_1960s.csv`.

```python3
outpath = "/sharedfolder/art_1960s.csv"

with open(outpath, 'w') as fo:
    csv_writer = csv.writer(fo)
    csv_writer.writerow(artwork_header)
    csv_writer.writerows(art_1960s_sorted)
```



```python3
outpath = "/sharedfolder/art_1960s.csv"
o = open(outpath, 'w')
a = csv.writer(o)
a.writerow(artwork_header)
a.writerows(art_1960s_sorted)
o.close()
```



Note that we call use `writerow` function first to write the header row, then `writerows` to write the actual data.

Find the new file in `sharedfolder` and open it in Excel or LibreOffice. Take a few moments to explore the collection.

![](week/3/Image-6.png)

#### The Dictionary Data Type

So far, when we want to access the “Artist” field in MoMA’s metadata, we’ve been referring to its position in a given row.

```python3
row = art_1960s_sorted[7700]
row[1]
```
 _Output:_

 ```python3
'Helen Frankenthaler'
```

This system is straightforward and well-suited for many jobs, but for large, complex projects it can be difficult to keep track of all those index numbers. Instead, we can use a dictionary to reference metadata fields by name rather than list index.

Just like we can refer to a item in a list using brackets to enclose its position in the list, a dictionary, or dict, uses any chosen string or number to identify a value in a collection. This data structure is known as a key-value pair. Here’s the simplest way to create a new dictionary.

```python3
artist_meta = {}
artist_meta['ConstituentID'] = 248
artist_meta['DisplayName'] = 'Richard Avedon'
artist_meta['ArtistBio'] = 'American, 1923–2004'
artist_meta['Nationality'] = 'American'
artist_meta['Gender'] = 'Male'
artist_meta['BeginDate'] = 1923
artist_meta['EndDate'] = 2004
artist_meta['Wiki QID'] = 'Q305497'
artist_meta['ULAN'] = '500013773'
```
The following is a more compact format for the same key-value assignment.

```python3
artist_meta = {'ConstituentID': 248, 'DisplayName': 'Richard Avedon', 'Gender': 'Male', 'BeginDate': 1923, 'EndDate': 2004, 'ULAN': '500013773', 'Wiki QID': 'Q305497', 'ArtistBio': 'American, 1923–2004', 'Nationality': 'American'}
```
To access a value, enter its key between brackets like so.

```python3
artist_meta['DisplayName']
```
And note that you can iterate over a dict to view and/or use its keys.

```python3
for key in artist_meta:
    print(key + " - " + str(artist_meta[key]))
```

Next, let’s create a dict for each artist MoMA’s artist metadata. Here’s a snippet (repeated from above) that loads `Artists.csv` as a list of lists called `artist_table`.

```python3
import csv

artist_csv_path = "/sharedfolder/Artists.csv"
artist_table = []

with open(artist_csv_path) as fi:
    csv_input = csv.reader(fi)
    for row in csv_input:
        artist_table.append(row)

artist_header = artist_table[0]
artist_table.remove(artist_table[0])

artist_header
```

Now we’ll use a for loop to iterate through `artist_table`, converting each list of cells to key-value format.

```python3
artist_dicts = []

for row in artist_table:
    artist_meta = {}
    artist_meta['ConstituentID'] = row[0]
    artist_meta['DisplayName'] = row[1]
    artist_meta['ArtistBio'] = row[2]
    artist_meta['Nationality'] = row[3]
    artist_meta['Gender'] = row[4]
    artist_meta['BeginDate'] = int(row[5])
    artist_meta['EndDate'] = int(row[6])
    artist_meta['Wiki QID'] = row[7]
    artist_meta['ULAN'] = row[8]
    artist_dicts.append(artist_meta)
```  

The list `artist_dicts` should now contain records for about 15,000 artists.

```python3
len(artist_dicts)
```
Specifying an index in brackets will return a dict object.

```python3
artist_dicts[12007]
```
And we can use one of our standard key names to get a particular value.

```python3
artist_dicts[12007]['DisplayName']
```
![](week/3/Image-7.png)

If we want to create a list of artist names, birth years, etc., we can thus iterate through the `artists_dicts` list and specify the field we want by name.
-->




<!--

Right click the following links and save the Jupyter notebook files to `sharedfolder` on your desktop.

1. [CSV Input/Output in Python](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/week-07.1_CSV-Input-Output.ipynb)

2. [Using the Google Books API](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/week-07.2_Google_Books_API.ipynb)

3. [Scraping and Parsing XML finding aids](https://raw.githubusercontent.com/pcda17/pcda17.github.io/master/Week-06_Scraping-and-Parsing-XML.ipynb)

Navigate to [localhost:8889](localhost:8889) in your browser to open each notebook.

Helpful hint: you may get an error if you are running a loop for a field that is empty. The good news is that you can add a safety net for this kind of eventuality using the statements "try" and "except" as you see in this example:

![](img/try.except.png)
-->
<!--

Open a new browser window and navigate to the Library of Congress's list of XML finding aids by collection: [http://findingaids.loc.gov/source/main](http://findingaids.loc.gov/source/main).

Choose a collection you would like to work with for today's class. For instance, the "Recorded Sound" collection is located at [http://findingaids.loc.gov/source/RS](http://findingaids.loc.gov/source/RS). Copy the URL of the page you've chosen.

Navigate to [localhost:8889](localhost:8889) in your browser to open Jupyter. In the `New` drop-down menu new the top right of the window, select `Terminal` to open a bash shell session in your browser.

Make a new directory in `/sharedfolder/` using the `mkdir` command, then `cd` into the directory.

```
mkdir LOC_Recorded_Sound

cd LOC_Recorded_Sound/
```

Download the LOC page you've chosen using `wget`. The `--adjust-extension` option adds ".html" to the end of the filename.

```
wget http://findingaids.loc.gov/source/RS --adjust-extension
```

> *Two more ways to download the contents of a web page:*
>
> - With the page open in your browser, go to `File > Save Page As ...` in the toolbar. In the window that pops up, select `Webpage, HTML Only` as your format, then save the file wherever you like.
>
> - Right click anywhere in the browser window and select `View Page Source`. A new browser tab will pop up to display the page's HTML source. Copy and paste the HTML into an empty text file.

In the macOS Finder or Windows Explorer, navigate to the `sharedfolder` directory on your desktop. Open the HTML file you just downloaded in `Atom`, or a text editor of your choice.

Scroll through the file and locate the list of links to finding aids. Each XML finding aid URL looks something like this: `http://hdl.loc.gov/loc.mbrsrs/eadmbrs.rs010001.2`

![](week/6/Image-0.png)

Our goal is to get each finding aid URL onto a separate line, using the text editor's "Find and Replace" feature.

Because the same series of characters appear before and after each URL — `href="` before and `" target=` after — use "Replace All" to replace each of these sequences with a newline.


![](week/6/Image-1.png)

![](week/6/Image-2.png)

Now save the HTML file (which is no longer proper HTML) and return to the terminal session in your browser.

We will now use the `grep` tool to search through the HTML file and extract lines containing URLS. The following command will write all lines in `RS.html` that include "http" to a new file called `url_list_1.txt`.

```
grep "http://" RS.html > url_list_1.txt
```

Open `url_list_1.txt` in your text editor and take a look. Note that the file still contains lines we don't need, including links to METS records, which end in `.4`. Since all finding aid URLs that we want end in `.2`, we can use `grep` again to extract just those URLs.

```
grep "\.2" url_list_1.txt > url_list_2.txt
```

Note that the `.` character in our `grep` search term needs to be escaped using a backslash.

Open `url_list_2.txt` in your text editor. If the file still contains any text other than the URLs we want, delete it by hand and save the file.

Now we're ready to download our collection of XML finding aids with `wget`. The `-i` option specifies that we want to download the files at every URL in a text file, with one URL per line.

```
wget -i url_list_2.txt
```

Navigate Jupyter Home at [http://localhost:8889](http://localhost:8889) and create a new Python 3 notebook.

In the first cell of your notebook, the following commands will change your working directory to `/sharedfolder/LOC_Recorded_Sound` and display a list of filenames in the directory.


```
import os

os.chdir('/sharedfolder/LOC_Recorded_Sound')

os.listdir('./')
```


Next we will use the BeautifulSoup package to parse an XML file. Insert one of your XML filenames in the snippet below and run it.

```
from bs4 import BeautifulSoup

xml_filename = 'eadmbrs.rs009003.2'

xml_text = open(xml_filename).read()

soup = BeautifulSoup(xml_text, 'lxml')
```

Open the same file in your text editor. Notice the tree structure of the XML file, in which each level of the XML tree is indented further than the one above it.

In case you're working with a XML or HTML file that isn't so neatly organized, this snippet will display a prettified version of the file.

```
from pprint import pprint

pprint(soup.prettify())
```

The following will locate the `author` element in the XML tree and display its contents.

```
author = soup.ead.filedesc.titlestmt.author.get_text()

print(author)
```

Or, more succinctly:

```
author = soup.find('author').get_text()

print(author)
```


The following snippet will print the `author` field for each file in your collection of finding aids:

```
for filename in [item for item in os.listdir('./') if item[-2:]=='.2']:
    page = open(filename).read()
    soup = BeautifulSoup(page, 'lxml')
    title = soup.title.string
    author = soup.find('author').get_text()
    print(author)
```


If an XML element type appears multiple times in a file, use `soup.findAll()` to return them in a list:

```
titles = soup.findAll('title')

print(titles)
```

To extract text from each element, you can use a for loop or, as below, a list comprehension:

```
titles = [item.get_text() for item in soup.findAll('title')]

print(titles)
```







### Crossref API

Crossref API format:

```
https://search.crossref.org/dois?q=10.5555%2F12345678
```

<!--
I just posted a Jupyter notebook that expands on what we did in class yesterday. It's a step-by-step demonstration of what it looks like to extract several metadata fields from a collection of XML files, then write everything to disk as a CSV file:

https://github.com/pcda17/pcda17.github.io/blob/master/Week-06_Scraping-and-Parsing-XML.ipynb (Links to an external site.)Links to an external site.

 (Links to an external site.)Links to an external site.

To run the notebook yourself, click "Raw" at the top right of the GitHub page to download the file. Once you add it to 'sharedfolder' on your desktop, open the Jupyter Home page (localhost:8889 (Links to an external site.)Links to an external site. while the Docker container is running) and click "Week-06_Scraping-and-Parsing-XML.ipynb" to open the notebook. To remove the output I've included under each cell, go to "Kernel > Restart & Clear Output" in the Jupyter toolbar.

You can find the CSV I created here:

https://github.com/pcda17/pcda17.github.io/blob/master/week/6/LOC_RS_Reduced_Metadata.csv?raw=true (Links to an external site.)Links to an external site.

Those XML finding aids are relatively messy and inconsistent, so the parsing process is a bit involved. I'd encourage you to take some time and try to understand each step.

-->

<!--


![](week/6/Image-.png)


![](week/6/Image-0.png)
![](week/6/Image-0.png)
![](week/6/Image-0.png)
### Class Objectives
- Download individual files, file lists, and entire websites using wget.
- Scrape structured data from Wikipedia.
- Access JSON data via APIs and re-formatting in tabular form.

#### Wget intro
We used Wget briefly in our first class, but today we’ll try out a few more advanced features. As we saw then, downloading the HTML source for a particular page is as easy as passing its url to Wget.

    wget http://example.com

 If we want to download a series of files, we can list their URLs in a text document and download them all using the `--input` or `-i` option. You can assemble a list yourself or try it out with [this](https://www.dropbox.com/s/e8quww6kixusflw/Ten_URLs.txt?dl=1) set of 10 random Wikipedia URLs.

    wget -i Ten_URLs.txt

Wget also supports recursive downloading. Download an entire website like so:

    wget ‐‐execute robots=off ‐‐recursive ‐‐no-parent ‐‐continue ‐‐no-clobber http://example.com/

You can also download a series of sequentially numbered files with following notation:

    wget http://example.com/images/{1..20}.jpg
    wget https://www.discogs.com/release/84319{10..25}


#### Beautiful Soup basics


#### In-Class Exercise: Scraping a Metadata Set from Wikipedia
- Choose a list of related Wikipedia articles (e.g., [The Top 100 Crime Novels of All Time](https://en.wikipedia.org/wiki/The_Top_100_Crime_Novels_of_All_Time)).
  - More options: [List of lists of lists](https://en.wikipedia.org/wiki/List_of_lists_of_lists#Literature)
- Download the list using Beautiful Soup and create a list of URLs for each page.
- Download each page on the list and extract relevant metadata (author, language, genre, publisher, date, page count, etc.).
- Export data as a CSV.

- Sample code for Wikipedia list scraping: [http://chrisalbon.com/python/beautiful\_soup\_scraping\_into\_pandas.html](http://chrisalbon.com/python/beautiful_soup_scraping_into_pandas.html)



#### ElementTree XML parser in Python

    import xml.etree.ElementTree as ET
    tree = ET.parse('/Users/yourname/Desktop/sandbox/country_data.xml')
    root = tree.getroot()

    for child in root:
        print child.tag, child.attrib

#### Discuss HTML, XML, and HTML5

#### Working with API Data
CrossRef metadata search:
- http://search.crossref.org/help/api
- http://search.crossref.org/dois?q=renear+palmer&sort=score
- http://search.crossref.org/dois?q=10.5555%2F12345678

-->

<!--
another set of code exercises separate from the top




#### Text I/O in Python
Now we’ll review reading and writing text files from the Python environment. Visit Project Gutenberg or the mirror provided and save the plain text version of Swift's *The Battle of the Books, and other Short Pieces* to your /sharedfolder on your desktop. It's a collection of essays, including a line Toole references in the title _A Confederacy of Dunces_.

- [http://www.gutenberg.org/ebooks/623](http://www.gutenberg.org/ebooks/623)
- [mirror](https://raw.githubusercontent.com/pcda17/pcda-datasets/master/week-02/pg623.txt)

First we’ll assign the file’s pathname to the variable `filepath` and create the file stream object we’ll use to read its contents. Open the Python shell and enter the following lines.

```
filepath = "/sharedfolder/pg623.txt"
file = open(filepath, encoding='utf8')
```

Then we’ll make an empty list called `swift_lines` and iterate through our file stream using a for loop, adding each line to the list as we go.

```
swift_lines = []
for line in file:
    swift_lines.append(line)
```

Finally, we’ll close our file stream and view a line from our list.

```
file.close()
swift_lines[1000]
```

> _Output:_
>
>     'flung by the assistance of so foul a goddess should pollute his fountain,\r\n'

**Tip:** In macOS you can drag a file from Finder to a Terminal window instead of entering the pathname by hand. If the path contains any spaces, these will be escaped (i.e., preceded by a backslash) in keeping with the conventions of Unix-like interfaces.
> Python’s `os` module, however, doesn’t recognize escaped characters. In order to avoid confusion, it’s probably best to avoid using spaces in filenames.
> If you are in our Docker Container, you will have to edit the pathname to reflect the /sharedfolder/ directory. For example, instead of this pathname:
>   "/Users/yourname/Desktop/Artists.csv"
> You would use this pathname:
>   "/sharedfolder/Artists.csv"

Each line ends with `\r\n` , a carriage return followed by a line feed character, suggesting the file was created in a Windows text editor. As Oualline and Noria discuss in this week’s readings, Unix-like systems generally use `\n` to indicate newlines, while `\r\n` is standard in Windows and DOS. To complicate matters, early Apple computers used `\r` on its own for the same purpose.

> **Tip:** While the term "newline" refers to any character or character combination used to mark the end of a line, when we say "newline character" for the rest of the course we’ll mean `\n` (formally called "line feed") unless otherwise noted.

![](week/2/Image-1.png)

Our text file from Project Gutenberg is broken into short lines, none longer than 74 characters. Many ASCII text files follow this fixed-width convention, designed to fit the 80-character width of many early PC displays. That display format, in turn, was chosen to work with data from 80-column punch cards, introduced by IBM in the 1920s.

Whether we’re adapting to quirks of history or fixing typing mistakes, we’ll often find it helpful to get rid of whitespace characters (newlines, spaces, tabs) at the beginning and end of a given string. For a string named `line`, `line.strip()` will return a copy of the string with all newlines and other whitespace characters removed from either end.

    line = swift_lines[1000]
    line
    line.strip()

#### Python Text I/O Continued

Closing a file stream with `close()` when you’re done with it is good style, though it’s not strictly required. If you want to keep your code compliant yet crisp, the following format closes a file stream automatically.

    swift_lines = []
    with open(filepath, encoding='utf8') as file:
         for line in file:
               swift_lines.append(line)

Or you can use this command, which does the same in one line.

    swift_lines = open(filepath, encoding='utf8').readlines()

Note that calling `readlines()` creates a list of all lines in a text file, including any newline characters (in this case, `\r\n` ). Let's take a look at 5 lines from our list.

    swift_lines[100:105]

> _Output:_
>
>     ["their after-life.  In July, 1692, with Sir William Temple's help,\r\n", 'Jonathan Swift commenced M.A. in Oxford, as of Hart Hall.  In 1694,\r\n', "Swift's ambition having been thwarted by an offer of a clerkship, of 120\r\n", 'pounds a year, in the Irish Rolls, he broke from Sir William Temple, took\r\n', 'orders, and obtained, through other influence, in January, 1695, the\r\n']

We could easily use a for loop with the `strip()` function to remove newlines from each string in the list, but the following line does the same in a shorter form. Here `open()` creates a file stream and `read()` returns the file’s contents as a single string. Finally, `some_text.splitlines()` returns a list of lines in the string `some_text`, removing newline characters along the way. Let's load the file using `splitlines()` and compare the results.

    swift_lines = open(filepath, encoding='utf8').read().splitlines()
    swift_lines[100:105]

> _Output:_
>
>     ["their after-life.  In July, 1692, with Sir William Temple's help,", 'Jonathan Swift commenced M.A. in Oxford, as of Hart Hall.  In 1694,', "Swift's ambition having been thwarted by an offer of a clerkship, of 120", 'pounds a year, in the Irish Rolls, he broke from Sir William Temple, took', 'orders, and obtained, through other influence, in January, 1695, the']

If we’d like to convert our list of lines to a block of flowable text, we can use `join()` to combine all items in the list `lines`, each separated by a space. Note that we end up losing the paragraph breaks we saw in the original file.

    swift_text = ' '.join(swift_lines)
    swift_text[10005:10223]

> _Output:_
>
>     "Satire is a sort of glass wherein beholders do generally discover everybody's face but their own; which is the chief reason for that kind reception it meets with in the world, and that so very few are offended with it."

#### Accessing Text Files on the Web

The Python module `urllib.request`  makes grabbing text from the Web as easy as working with local files. Let’s download the first two chapters of _A Confederacy of Dunces_ in plain ASCII format.

```
from urllib.request import urlopen
url = "https://raw.githubusercontent.com/pcda17/pcda-datasets/master/week-02/Toole_A-Confederacy-of-Dunces_Ch1-2.txt"
toole_lines =  urlopen(url).read().decode('utf8').splitlines()
```

Let’s look at the 200th line in the file.

    toole_lines[199]

> _Output:_
>
>     'Ignatius had himself broken the baseball machine by kicking it.'

Since we’ll be doing a lot of text filtering this semester, you should get used to checking whether a string includes a specified substring. Enter the following lines and press return twice. The first return brings us to a new line and lets us add more indented code if we choose to. The second confirms we've finished our conditional statement and runs it.

    if "Reilly" in "Ignatius J. Reilly":
         print("yes")

To do a case-insensitive substring search, use the `lower()` function to convert your original string to lowercase. If your search term contains any capital letters, you’ll want to convert it to lowercase as well.

    if "reilly" in "Ignatius J. Reilly".lower():
         print("yes")

Try creating a simple text filter or two, printing all lines that contain a given substring. Run these examples one at a time, then search for a word of your choice.

```python3
for line in toole_lines:
    if "orleans" in line.lower():
        print(line)

for line in toole_lines:
    if "doughnut" in line.lower():
        print(line)
```

While you’re at it, use a for loop to identify the sentence by Jonathan Swift (in `swift_lines`) that Toole references in his title _A Confederacy of Dunces_. Try to resist the urge to use ⌘+F in TextWrangler.

#### Defining Functions

We talked a bit about functions last week, but let’s review. Note that when you define a function in the Python shell, pressing return once will move you to the next line within the function-in-progress. Hit return again to finish the function definition and return to the standard Python shell.

Here is a simple function that multiplies a number (float or int) by itself.

```python3
def square(number):
     return number * number

square(11)
```

Note that functions can be nested within one another. The following will call the `square` function twice.

    square(square(11))

We can also create functions that take two or more arguments.

```python3
def multiply(x,y):
    return x * y

multiply(4,6)
```

And here’s an example of a function that manipulates string data.

```python3
def pluralize(string):
     return string + 's'

pluralize("eagle")
```

> **Tip:** There’s a difference between ending a function with `return` as opposed to `print`. Using "return" allows you to assign function output to a variable or pass it to another function, while "print" simply displays text in the Python shell.

Python is weakly typed, meaning intended data types don’t need to be specified in advance when we create a function. Applying an operation to a value of the wrong type will produce an error.

    square("eagle")
    pluralize(1960)

Using the `str`, `int`, and `float` functions, we can cast values as string, int, or float data types (when doing so is possible).

```python3
def pluralize(string):
     print(str(string) + 's')

pluralize(1960)
```

#### Generating pseudorandom numbers
It is often useful to generate random numbers or make random selections from a set of data. Note that Python can’t generate a mathematically pure sequence of random values; instead, it creates what are called "pseudorandom" values. Details of the difference are beyond the scope of this course, but when we use the term "random" below we really mean "pseudorandom."

Import the `random` module and generate a random float X, where 0 \<= X \< 1.

    import random
    random.random()

Return a random integer from 0 to 49.

    int(random.random() * 50)

This is equivalent to the following:

    random.randint(0,49)

Note that `randint` is inclusive, so it may output 49, the second argument we passed it.

#### Quick Assignments
Assign a list of strings to a variable — in this case, a collection of foods mentioned in Toole’s novel.

    foods = ['macaroon', 'hot dog', 'jelly doughnut', 'Dr. Nut', 'wine cake', 'Dutch cookies', 'stuffed eggplant', 'jumbalaya with shrimps', 'brownie']

_Assignment:_ Write a function that accepts a list of strings and returns a randomly chosen value.

> _A possible solution:_
>
>     def random_choice(list):
>          return list[int(random.random()*len(list))]
>     
>     random_choice(foods)


_Assignment:_ Create a new function that returns a list of 3 randomly chosen strings. Don’t worry about repetitions.

> _A possible solution:_
>
>     def random_three(list):
>          temp_list = []
>          for i in range(3):
>                temp_list.append(random_choice(list))
>          return temp_list
>     
>     random_three(foods)

_Assignment:_ Modify the function to return a list of 3 random strings containing the letter "a." Don’t worry about repetitions.

> _A possible solution:_
>   
>    def random_three_with_a(list):
>         temp_list = []
>         while(len(temp_list)<3):
>               temp_choice = random_choice(list)
>               if 'a' in temp_choice:
>                     temp_list.append(temp_choice)
>         return temp_list
>   
>    random_three_with_a(foods)

As you might expect, Python provides tools to speed up the work you just did by hand. The following returns a single randomly selected item from a list.

    random.choice(foods)

This command returns a list of three random selections without repetition.

    random.sample(foods,3)

And this one shuffles the order of a list’s contents, overwriting the original list.

```
random.shuffle(foods)    

foods
```

#### Random Word

Now let’s choose a random word from the English lexicon. Most Unix-like systems include a standard word list called `words`, which some programs use  (or used to use) for spell checking. Let’s assign the pathname for `words` to the variable `word_path`, then load the file as a list of individual words.

```
words_path = "/usr/share/dict/words"
words = open(words_path).read().splitlines()
```

Let’s check the length of our lexicon. It should be over 150,000 words.

```
len(words)
```

Enter the following to generate a list of 50 random words.

```
random.sample(words,50)
```

Is there anything notable about the words in this random list? If so, how might you explain the pattern?

#### Text Processing Oddities

By this point you’ve likely noticed that text strings can be enclosed in single quotes (`'Miss Trixie'`) or double (`"Patrolman Mancuso"`) at the coder’s discretion.

If we use double quotes, our string can contain single quote characters without ambiguity. Note that the first line below returns an "invalid syntax" error, while the second is successful.

```
some_text = 'How I'm supposed to know who's a cop? Everybody looks the same to me.'

some_text = "How I'm supposed to know who's a cop? Everybody looks the same to me."
```

Likewise, single quotes can be used to assign a string containing double quotes.

    some_more = '"We goin back to the factory," the spokesman for the choir, the intense lady, said angrily to Ignatius. "You a bad man. I believe a po-lice looking for you."'

To include newline characters and/or any combination of single and double quotes, Python lets us bound strings with triple quotes (i.e., three single quotes in a row). Copy the entire code block below and paste it into the Python shell.

```
even_more_text = '''"My," Ignatius said to the old man after having taken his first bite. "These are rather strong. What are the ingredients in these?"

"Rubber, cereal, tripe. Who knows? I wouldn't touch one of them myself."

"They're curiously appealing," Ignatius said, clearing his throat. "I thought that the vibrissae about my nostrils detected something unique while I was outside."

Ignatius chewed with a blissful savagery, studying the scar on the man's nose and listening to his whistling.'''
```

<!--
By default, Python 3 string objects represent text using 8-bit ascii, a version of a bare-bones text encoding format dating back to the 1960s. Python also supports 16-bit Unicode (UTF-16), a more recent standard that includes ~120,000 characters from a vast array of contemporary and historical scripts, as well as symbol sets including abstract shapes and every emoji. In Python, Unicode strings are immediately preceded by the letter `u`.

    ascii_text = "This is an ASCII string."
    unicode_text = u"This is a Unicode string."
    ascii_text
    unicode_text

Note that we can cast Unicode text to ASCII with the `str()` function.

    str(unicode_text)
-->
<!--

#### Quick Exercises

_Exercise:_ Download a text file from Project Gutenberg and print 14 randomly chosen lines.

> _A possible solution:_
>
>     url = "https://raw.githubusercontent.com/pcda17/pcda-datasets/master/week-02/pg623.txt"
>     swift_lines = urlopen(url).read().decode('utf8').splitlines()
>     
>     random_lines = random.sample(swift_lines,14)
>     
>     for line in random_lines:
>          print(line)


_Exercise:_ Modify your code to return 14 random lines containing a chosen word or phrase.

> _A possible solution:_
>
>     url = "https://raw.githubusercontent.com/pcda17/pcda-datasets/master/week-02/pg623.txt"
>     swift_lines = urlopen(url).read().decode('utf8').splitlines()
>     
>     swift_she = []
>     
>     for line in swift_lines:
>          if "she" in line.lower():
>                swift_she.append(line)
>     
>     for line in random.sample(swift_she,14):
>         print(line)

_Exercise:_ Try using a different text and compare the results.

> _A possible solution:_
>
>     url = "http://www.gutenberg.org/cache/epub/14328/pg14328.txt"
>     boethius_lines = urlopen(url).read().decode('utf8').splitlines()
>     
>     boethius_she = []
>     
>     for line in boethius_lines:
>          if "she" in line.lower():
>                boethius_she.append(line)
>     
>     for line in random.sample(boethius_she,14):
>         print(line)




#### View list of all installed Python modules

Enter the following command to enter Python’s help shell.

    help()

Now enter the following and press return. After a moment, Python will display a list of all available modules.

    modules

Enter the name of a module and press return to view its help page, including a list of the module’s functions and other resources.

    random

![](week/2/Image-5.png)

Press `q` to close the help page, then hit return to get back to the Python shell. You can jump straight to module’s help page by passing its name to the `help()` function.

    help('random')

Or if the module is already imported, you can refer to the module itself.

    import random
    help(random)

To view a pared-down list of module resources, use the `dir()` function instead.

    dir(random)

![](week/2/Image-6.png)

The result is a challenge to read through, so let’s introduce the `pprint`, or "pretty-print" module.

```
from pprint import pprint
pprint(dir(random))
```

![](week/2/Image-7.png)

`pprint` displays one item from the list per line, a much more readable format. We won’t mention `pprint` often in these tutorials, but keep it in mind for your own future use.


#### The `os` module
The `os` library contains many useful tools for working with local files and even issuing commands directly to the system shell. We’ll start by importing the `os` module, navigating to the desktop, and creating a list of the directory’s contents.

    import os
    os.chdir("/sharedfolder/")
    file_list = os.listdir("./")
    file_list

<!--
> **Tip:** The `os` library won’t recognize the `~/` shortcut for a user’s local files. Instead, we can use `os.path.expanduser('~/path/to/file.txt')`.
-->

<!--

The `os.system` function lets us issue commands at the level of the system shell. The following example will print the contents of your desktop. Note that whereas `os.listdir()` returns a list object containing filenames, the following simply displays a list of files as if you were using the Bash shell.

    os.system("ls /sharedfolder/")

> **Tip:** Spaces in filenames are handled differently in `os.chdir()` and `os.system()`. In the latter case they must be escaped (preceded by a backslash) in keeping with Unix conventions, while in the former escaped spaces will generate errors. For convenience, it’s helpful to avoid spaces in filenames.



#### Downloading Reviews from Amazon (the hard way)

Start a new Python 3 notebook by going to `File/New Notebook` in the Jupyter window.

Enter the following in a cell.

```python3
from urllib.request import urlopen
url = "http://www.amazon.com/Confederacy-Dunces-John-Kennedy-Toole/dp/0802130208"
page = urlopen(url).read().decode('utf8')

print(page)
```

To make things simple, let's chop off the top of the page. Find a piece of text that only appears between the product details and the reviews — "Top customer reviews" is a good example — and use `split()` to make a list with two elements. Then assign the second chunk (at index 1) to the `page` variable.

```
page_bottom = page.split("Top customer reviews")[1]
```

Now let's chop off the bottom of the page the same way.

```
page_middle = page_bottom.split("Set up an Amazon Giveaway")[0]
```

Next we’ll split the remaining text into individual reviews. Note that the "review rating" HTML class is used at the beginning of each review. We’ll split our page
at those points, using triple quotes to include the end of the HTML tag.

```
review_list = page_middle.split('''review-rating">''')

print(review_list[0])
```

Since the first item in our list of segments comes before the first review, we’ll remove it using list index notation.

    review_list = review_list[1:]

Now the first element of our list should begin with a review.

    print(review_list[0])

Now let’s remove the code following each review. Since the text "Was this review helpful to you?" appears after every review, let’s use that as our delimiter. We’ll split each segment at that point and discard everything that follows it using list bracket notation.

```python3
review_list_2 = []

for review in review_list:
     review_list_2.append(review.split("Was this review helpful to you?")[0])

test_review = review_list_2[0]
print(test_review)
```

Now that our reviews are roughly cut down to size, let’s clean them up by removing HTML tags. The following function uses Python’s `re` module for working with regular expressions to replace any text between `<` and `>` with a newline. We’ll talk more about regular expressions later in the course.

```
import re

def strip_html(data):
    p = re.compile(r'<.*?>')
    return p.sub('\n', data)
```

Let’s see an HTML-free version of the segment we looked at above.

```
strip_html(test_review)
```

Note that there are multiple newlines between fields of interest, each one corresponding to a tag that’s been removed. Since we’d like to create a list of fields, we could use `split('\n')` to divide the text at each newline character — but then we’d also break up reviews with multiple paragraphs. Instead we’ll use pairs of newlines as our delimiter.

```
test_review_segments = strip_html(test_review).split('\n\n')

print(test_review_segments)
```

We’re getting there, but our list contains some empty strings and several entries may begin with newline characters. We can take care of these issues with a for loop, creating a new list that excludes empty strings and applies `strip()` to remove whitespace from each field we add.

```python3
final_review_segments = []

for item in test_review_segments:
     if item != '':
           final_review_segments.append(item.strip())

print(final_review_segments)
```


#### In-Class Exercise

Open your text editor of choice. Drawing on the code examples above, create a script that accepts a URL and produces a list of lists, one for each review on the page. A good strategy is to split the work between two functions: one that accepts a segment of the text and code (such as `test_review` above) and returns a cleaned-up list of fields, and a second that converts a review and its surrounding code to a list of segments.

You can use the `html_stripper()` function above or modify it at will.


> _A possible solution:_
>    
>     from urllib.request import urlopen
>     from pprint import pprint
>     
>     import re
>     def strip_html(data):
>         p = re.compile(r'<.*?>')
>         return p.sub('\n', data)
>     
>     def review_to_list(review):
>         temp_list = strip_html(review).split('\n\n')
>         review_list = []
>         for item in temp_list:
>              if item != '':
>                 review_list.append(item.strip())
>         return review_list
>     
>     def page_to_table(url):
>         page = urlopen(url).read().decode('utf8')
>         page_bottom = page.split("Top customer reviews")[1]
>         page_middle = page_bottom.split("Set up an Amazon Giveaway")[0]
>         review_list = page_middle.split('''review-rating">''')
>         review_list = review_list[1:-1]
>         review_list_2 = []
>         for review in review_list:
>              review_list_2.append(review.split("Was this review helpful to you?")[0])
>         table = []
>         for review in review_list_2:
>              table.append(review_to_list(review))
>         return table
>    
>     url = "http://www.amazon.com/Confederacy-Dunces-John-Kennedy-Toole/dp/0802130208"
>     review_table = page_to_table(url)
>    
>     pprint(review_table)
>    
>     import csv
>    
>     outpath = "/sharedfolder/amazon.csv"
>     o = open(outpath, 'w')
>     a = csv.writer(o)
>     a.writerows(review_table)
>     o.close()




<!--
## Demonstrate server-side Python script
- Create a text file containing Python code to print "Hello world!"
- Add shebang line at top of file:

```
  #!/usr/bin/env python3
```

- Name the file `page.html.py`
- Upload file to server and set file permissions to 755.
- Open URL in browser.
-->

<!--
#### Optional Exercise: Podcast this Directory
Working in pairs, create a server-side script that detects mp3 files in a given directory and creates an podcast RSS feed from the list.
- Example podcast feed: [https://www.dropbox.com/s/x5ubi18086eod9n/simple\_podcast.rss?dl=0](#)
- Example solution: [Link](#)
-->
