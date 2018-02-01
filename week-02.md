## Week 2: Python Intro

### Objectives
- Defining data models
- Using Docker
- Programming basics in Python
- Launching Jupyter
- Defining basics
- String manipulation

#### Defining data models
See [Python glossary on data models](https://docs.python.org/3/reference/datamodel.html)

#### Using Docker
Open a new terminal window.

View all current Docker containers:

```python
docker ps -a
```

Close and remove the container we started last time if it's still open, use `docker rm -f` followed by its name, like so:

```python
docker rm -f pcda_ubuntu
```

To close and remove all current Docker containers, enter the following command:

```python
docker rm $(docker ps -aq)
```

Enter the following command in the terminal window to download the Docker image files we'll be using. This could take several minutes.

```python
docker pull pcda17/ubuntu-container
```

When the download is complete, enter the following command to run the container. This will create or be directed to your new directory called `sharedfolder` on your desktop.

```python
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container bash
```

#### Programming basics in Python
To get started using Python, simply enter `python3` in the shell.

python3

We’ve just switched from the standard shell to the Python environment, which you can tell at a glance by the “\>\>\>” to the left of your cursor. We’re in what’s known as a language shell or a read-eval-print loop (REPL), in which any commands we enter will be interpreted as Python code. You can leave Python at any time by entering the `quit()` command.

We’ll begin by assigning some data to variables.
```python
x=5
y=5.0
z="Hello"
```
If you type `x` and hit return, you’ll notice the variable’s current value is output on the line below. Trying the same with `x+2` will return 7.
```python
x+2
```
Note that `x+x` gives a result of 10, while `x+y` returns 10.0. That’s because 5 and 5.0 are different data types in Python. The former is an **int**, or integer, while the latter is a **float**, or floating point value.

Now try using the `+` operator on two strings.
```python
z+" world"
```
> Output:
>
> 'Hello world'

Note that `+` is used for two entirely different purposes: adding numbers and concatenating strings. When the same symbol performs multiple tasks in different contexts, it’s described as overloaded.


Next we’ll link a series of values using Python’s list data type. There several ways to represent an ordered sequence of items in Python, but we’ll be using list most frequently.

```python
eu_countries=['Austria', 'Belgium', 'Bulgaria', 'Croatia', 'Republic of Cyprus', 'Czech Republic', 'Denmark', 'Estonia', 'Finland', 'France', 'Germany', 'Greece', 'Hungary', 'Ireland', 'Italy', 'Latvia', 'Lithuania', 'Luxembourg', 'Malta', 'Netherlands', 'Poland', 'Portugal', 'Romania', 'Slovakia', 'Slovenia', 'Spain', 'Sweden', 'UK']
```

We can now refer to individual list members using bracket annotation.

```python
eu_countries[3]
```
The command above returns the string “Croatia,” which is located at index 3. As in most programming languages, we begin counting from 0 when working with ordered data.

If you try to access an out-of-range index value you’ll get an error.

```python
eu_countries[99]
```
We can also create a subset of a list using Python’s slice notation. The following will return a list containing four items, beginning at index 3 in `eu_countries`.

```python
eu_countries[3:7]
```
Leaving one side of the colon blank will include all items on that end of the list.
```python
eu_countries[5:]
eu_countries[:10]
```
We can also use negative numbers to count backwards from the end of a list. The following will return “UK,” the final string in the list.
```python
eu_countries[-1]
```
Under the hood, every string in Python is actually a list of individual characters. In the example below, `word[7]` returns the letter “e,” while `word[7:20]` returns “establishment.”
```python
word="antidisestablishmentarianism"
word[7]
word[7:20]
```
If we need to know the length of a list or string, the `len` function can tell us.
```python
len(eu_countries)
len(word)
```
Conditional statements are a fundamental part of all programming languages. We use the `if` operator to evaluate conditionals.

> **Tip:** It is significant in Python to use the tab when you see a tabbed space in the code such as in the example below. Below, you will be given a new line after the colon `:`  but you will still need to tab once before typing the `print` command or you'll get an error. Further, you must hit 'return' twice after the final line to run the piece of code.

```python
number=12
if number==12:
    print("The value is 12, an integer.")
```

By adding `else`, we can tell Python to do something if the conditional isn’t true.
> **Tip:** The tabs can be kind of tricky with this one. In this example, be sure to tab once before each `print`  command.

```python
number=10
if number==12:
    print ("The value is 12, an integer.")
else:
    print ("The value is not 12.")
```

A **for loop** is a structure that lets us iterate through lists and other data structures so we can refer to each item one at a time.
```python
for country in eu_countries:
    print(country + ' is great.')
```
Finally, we can create functions to automate repetitive processes. Use the `def` declaration to start s function definition. The code below will produce the same output as the last example.

```python
def is_great(word):
    return word + ' is great.'

for country in eu_countries:
    print(is_great(country))
```

In this case we’re not saving much effort, but as we proceed you’ll find that functions will help you write simpler, more readable code.


#### Launching Jupyter
First, leave the Docker terminal (ctrl+p, then ctrl+q, like we did at the end of last week). Restart the Docker container to run a browser instead of a Terminal application so that we can launch Jupyter:

```python
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container
```
Windows 10 version:
```python
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume C:\Users\***username_here***\Desktop\sharedfolder:/sharedfolder/ pcda17/ubuntu-container
```

Open any browser and type (your Juypter Notebook will launch):

```python
localhost:8889

```
![](week/2/Image-1.png)

Click the "New" in the upper right, then choose "Python 3" from the drop-down menu.

![](week/2/Image-2.png)

![](week/2/Image-3.png)

You’re now in the Jupyter environment. Here, you can create a series of "cells" for individual chunks of code, which can be saved and run repeatedly. Click the ✚ icon on the top left to add a new cell.

Type a line of code that prints a string. To run the current cell, either click the `►❙` icon or go to the "Cell" menu and choose "Run Cells."
```python
print("Hello Jupyter!")
```
![](week/2/Image-4.png)

Note that each cell’s output is displayed right below to the the code that produced it, which is a major benefit of working in Jupyter.

### Exercises
Right click the following link and save the Jupyter notebook file to `sharedfolder` on your desktop.
[Karsdorp, Chapter 1:](http://nbviewer.jupyter.org/github/fbkarsdorp/python-course/blob/master/Chapter%201%20-%20Getting%20started.ipynb)
Do *Defining basics* through *String manipulation*

### More exercises

Assign a sentence to the variable `sentence` — in this case the opening line from John Kennedy Toole’s  _A Confederacy of Dunces_. Type the name of the variable and hit shift-return to view your new string.

```python
sentence="A green hunting cap squeezed the top of a fleshy balloon of a head."

sentence
```

**Output:**

    A green hunting cap squeezed the top of a fleshy balloon of a head.

Making lists happens more often than any other data structure, so it’s worth reviewing the details of Python’s slice notation. Let’s create a list of strings, then view a subset of the list to a new variable. Enter the variable “words2” to view the result.
```python
words=['A', 'green', 'hunting', 'cap', 'squeezed']
words2=words[2:4]
words2
```

The Python shell should print `['hunting', 'cap']`, i.e., the subset of the list “words” from index 2 to index 3. In general, `list_name[start:end]`, where “start” and “end” are integers, returns a subset of “list-name” from index `start` to `end-1`. The “end minus 1” bit may seem odd, but in practice it makes slice notation more readable. The snippet above, for instance, gives us a list containing 2 items, equal to 4-2. And if we want to excerpt the first three items in a list, the following notation will do the trick.
```python
words[:3]
```

Recall that omitting an index number before or after the colon means you want to include all items on that end of the list. The following returns everything from index 2 to the end of “words”: `['hunting', 'cap', 'squeezed']`.
```python
words[2:]
```
If you want to excerpt the last three entries in a list without counting from the beginning, use a negative number before the colon.
```python
words[-3:]
```

Likewise, the following will slice off the final 3 items in our list, returning `['A', 'green']`.
```python
words[:-3]
```
To reverse the order of a list, add an extra colon and “-1.”
```python
words[::-1]
```
It’s important to note that in Python, every string is a list of characters under the hood. We can thus reverse the spelling of a sentence like so.
```python
sentence="A green hunting cap squeezed the top of a fleshy balloon of a head."
sentence[::-1]
```
If want to break our sentence into words, we can use the `split()` function to create a list of substrings with the space character as delimiter.
```python
words=sentence.split(' ')
words
```
The `join()` function reverses the process, inserting a chosen string (here, a space) between each item in a list. Note that “sentence2” below is identical to our original “sentence” string.
```python
sentence2=' '.join(words)
sentence2
sentence
```
<!--
#### Quick Exercise
Using the techniques outlined above, reverse the order of words in our sentence and combine them into a single string.

> _A possible solution:_
>
> ' '.join(sentence.split(' ')[::-1])
-->
Another useful string function is `replace()`, which lets us swap out one substring for another.
```python
sentence3 = sentence.replace('hunting','baseball')
sentence3
```
Finally, note that a number can be represented as one of three data types: integer, float, or string.
```python
sample_int = 35
sample_float = 35.4
sample_string = '35'
sample_int
sample_float
sample_string
```
We can convert among these formats using the `int()`, `float()`, and `str()` functions. After assigning the values below, enter each variable’s name and be sure you understand the result.
```python
cast_int = int(35.4)
cast_float = float(35)
cast_string = str(35)
cast_int
cast_float
cast_string
```
A string that includes only numbers and possibly a decimal point — no commas or other characters — can also be cast to the int or float data type.
```python
x = int('75')
y = float('107.5')
x
y
```
