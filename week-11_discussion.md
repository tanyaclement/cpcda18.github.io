## Week 11: discussion

#### Working with JSON
JSON data is a representation of key-value pairs, very much like a dictionary in Python. For the following example we’ll download a JSON version of the artwork metadata we’ve been working with.

```python3
import json
from urllib.request import urlopen

url = "https://media.githubusercontent.com/media/MuseumofModernArt/collection/master/Artworks.json?raw=true"
json_string = urlopen(url).read().decode('utf8')
json_data = json.loads(json_string)
```
To view JSON data (as well as dictionaries and just about any other data format), Python offers a “pretty printer” module. Here we are viewing the first 200 artworks in the metadata set.

There are also numerous online tools for prettifying JSON data, such as [these](http://jsonviewer.stack.hu/) [two](http://json.parser.online.fr/beta/).

```python3
from pprint import pprint

pprint(json_data[:200])
```

Much like a dictionary object in Python, a JSON object is made up of key-value pairs that can contain (and be contained in) lists. In this case, MoMA has presented metadata for its artworks as a list of key-value pairs.

To see the number of artworks included in the JSON object, use the `len()` function.

```
len(json_data)
```

To view the key-value metadata for a random artwork, use `random.choice()`.

```
import random

random.choice(json_data)
```

Using bracket notation, we can access individual metadata fields by their keys. Here we display several metadata fields for a randomly chosen artwork.

```
artwork = random.choice(json_data)

print(artwork['Artist'])
print(artwork['Title'])
print(artwork['Date'])
print(artwork['ObjectID'])
print(artwork['URL'])
```

The following loop will print the `Artist` field for the first 100 artworks in the list.

```python3
for item in json_data[:100]:
    pprint(item['Artist'])
```

You can also use `random.sample()` to view artist names for 100 artworks chosen at random.

```
for item in random.sample(json_data, 100):
    pprint(item['Artist'])
```

#### JSON Data to CSV
Next we’ll transfer these metadata fields to CSV format. First, let’s print a list of metadata fields for reference:

```python3
header = []

for key in json_data[0]:
    header.append(key)
```

Next we'll create a list of metadata fields to include in our CSV. These keys will appear at the top of the file as column headers.

```
column_headers = ['Date', 'Artist', 'Title', 'Medium', 'Nationality', 'ObjectID', 'URL', 'Department']

pprint(column_headers)
```
Then we’ll use these keys to create a list of rows for our CSV. Since some metadata entries in the JSON object appear as lists rather than strings, we’ll use the `str()` function to reformat each metadata item as we add it to the table.

To avoid slowing things down, we will work with metadata for 20,000 randomly chosen artworks.

```python3
meta_table = []

for record in random.sample(json_data, 20000):
    row = []
    for key in column_headers:
        row.append(str(record[key]))
    meta_table.append(row)

pprint(meta_table[0])
```

Finally, we will write our metadata list of lists as a CSV.

```python3
import csv

out_path = "/sharedfolder/MoMA_20K.csv"

with open(out_path, 'w') as fo:
    csv_out = csv.writer(fo)
    csv_out.writerow(column_headers)
    csv_out.writerows(meta_table)
```

Open your CSV in LibreOffice or Excel.


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
