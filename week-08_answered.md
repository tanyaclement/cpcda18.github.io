## Week 8 answered


#### Quick Assignment 1
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
#### Quick Assignment 2
Write a piece of code that creates a new table (i.e., list of lists) containing only artists born in the 1880s.

 _A possible solution:_

```python3
born_1880s = []

for row in artist_table:
    if 1880 <= int(row[5]) <= 1889:
        born_1880s.append(row)
```

#### Quick Assignment 3
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

#### Quick Assignment 4
Returning to our original MoMA metadata table, write a piece of code that extracts only works created in the 1960s (or another decade of your choosing). Since the date field in MoMA’s metadata doesn’t follow a strictly defined numerical format, you’ll have to think about how to interpret values like “1963,” “1963-5“, “c. 1963,” “c. 1960s,” etc.
<!--Let students struggle with this a bit, then encourage them to settle on a relatively quick and dirty solution. The collection doesn’t have to be perfect; we’ll be cleaning the table in OpenRefine later.-->

 _A simple solution with high recall and low precision:_

```python3
art_1960s = []

for row in artwork_table:
    if '196' in row[8]:
        art_1960s.append(row)
```

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
