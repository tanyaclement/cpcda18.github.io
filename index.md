<!--
Notes:
Best, Stephen, and Sharon Marcus. “Surface Reading: An Introduction.” Representations, vol. 108, no. 1, 1 Nov. 2009, pp. 1–21. JSTOR, doi:http://dx.doi.org/10.1525/rep.2009.108.1.1.

Manipulating strings, replacing and splitting
list comprehensions
working with lists, slice notation,
different data types: integer, float, string, can't mash them together, boolean true and false values; different lists in python.

-->
# Critical Perspectives in Cultural Data Analysis

#### University of Texas at Austin School of Information

Spring 2018, Mondays 3–6 p.m. UTA 1.210A

Instructor: Tanya Clement

Office hours: Mondays 1–3 p.m., UTA 5.558

## Course Schedule

[Week 1](#week1) | [Week 2](#week2) | [Week 3](#week3) | [Week 4](#week4) | [Week 5](#week5) | [Week 6](#week6) | [Week 7](#week7) | [Week 8](#week8) | [Week 9](#week9) | [Week 10](#week10) | [Week 11](#week11) | [Week 12](#week12) | [Week 13](#week13) | [Week 14](#week14)

## Course Objectives

Prerequsites: advanced-level undergraduate or graduate coursework in the humanities; no or very little programming experience preferred;

In the data, information, knowledge, wisdom (DIKW) hierarchy that circulates through Knowledge Management (KM) and Information Science (IS) discussions, data appears at the base of a pyramid of which wisdom is the pinnacle. In this schematic, data is “raw” and lacking in meaning, while information, the next higher level of the pyramid—just below knowledge and then wisdom—represents the presence of added links and relationships; information is higher up on the wisdom chain because it is data made meaningful. In the humanities, students are taught that data is not found in the “raw” but has rather been cooked all along, taken and constructed and seasoned according to our situated contexts including access issues (Where is the data?); media, format, and technology constraints (How is the data?); and perspectives (What is the data? Who is involved in and impacted by its creation and use?).

Learning to think critically about data as information means rejecting common illusions about data more generally, including its objectivity, impersonality, atemporality, and authorlessness. To teach students to think about information from this more critical perspective means first understanding how a culture tends to understand what is informative.

The aim of this course is to encourage students to generate high quality scholarship that applies computational and quantitative methods to the study of cultural artifacts (text, image, sound) at significantly larger scales than traditional methods. The final research paper is expected to combine critical theory, computational methods, and grounding in a particular humanities field towards the crafting of novel, thought-provoking arguments in the humanities.

Towards these ends, this course takes on “data wrangling” in the context of humanist perspectives.

Learning goals:

-  Exploring the cultural implications of large-scale data analysis with cultural materials.

-  Writing using perspectives in critical data studies;

-  Gaining familiarity with scripting-style programming in Python and Unix-like systems with an emphasis on gaining critical perspectives on the  use of freely available data sets in the humanities and on free and open source software; in techniques for collecting, transforming, and analyzing media and metadata available on the Web; of commonly used data models and their standard formats, including CSV, JSON, and XML; of text analysis techniques such as natural language processing (NLP), sentiment analysis, and machine learning classification; and with tools for analyzing cultural data via visualization and statistical tests

## Course Principles

-  Writing critically about data requires both a level of knowledge about data and data wrangling as it requires a level of knowledge about thinking and writing from critical perspectives learned in cultural studies. While this course does not *teach* cultural studies per se, an understanding of and experience in humanities theory and research and the principles of cultural studies are essential for success in the course.

-  Imitating and modifying others’ code is essential in learning to program. You can many examples and explanations on [Stack Exchange](http://stackexchange.com) and similar online forums. Taking one or two lines without attribution is OK; if you use a longer chunk of code found online, add a #comment with the source’s URL.

-   Begin assignments early. If you realize what you had in mind is more difficult than expected, talk to the instructor about choosing an alternative.

-   We’ll be focusing on a scripting approach to programming. This course is not oriented toward developing large, complex programs or writing perfectly optimized code.

-   Learning to code takes trial and error. Work through weekly programming tutorials before class and continue polishing in-class coding assignments at home.

## Course materials

There is one required text for this course:

_Montfort, Nick. Exploratory Programming for the Arts and Humanities. Cambridge, MA: The MIT Press, 2016._

All other readings will either be available online and linked below or [posted on Canvas](https://utexas.instructure.com/courses/1216881/files).

## Assignments
### [Class Attendance and Participation (10%)](https://utexas.instructure.com/courses/1216881/assignments/4276538)
### [Discussion Lead (5%)](https://utexas.instructure.com/courses/1216881/assignments/4276501)
### [Weekly Discussion Posts (30%)](https://utexas.instructure.com/courses/1216881/assignments/4240876)
### [Data Set Review (15%)](http://culturalanalytics.org/2017/10/introducing-data-sets-a-new-section/)
### [Final Project: Critical Data Analysis Research Paper (40%)](https://utexas.instructure.com/courses/1216881/assignments/4240878)

----------------------------------------------------------------
# I. Cultural Data Analysis

## <a name="week1"></a>Week 1 (1/22): Introduction to Cultural Data Analysis

### Readings
- danah boyd & Kate Crawford (2012) "Critical Questions for Big Data," *Information, Communication & Society*, 15:5, 662-679.
- Piper, Andrew. "There will be Numbers." *Journal of Cultural Analytics* 1, no. 1 (May 23, 2016). [http://culturalanalytics.org/2016/05/there-will-be-numbers/](http://culturalanalytics.org/2016/05/there-will-be-numbers/)
- Bod, Rens. "Introduction: the Quest for Principles and Patterns." *A New History of the Humanities: The Search for Principles and Patterns from Antiquity to the Present.* Oxford University Press, 2013, pp. 1 - 12. *Note: You must be logged in as a UT student to retrieve this text*: [http://catalog.lib.utexas.edu/record=b8902003~S29](http://catalog.lib.utexas.edu/record=b8902003~S29)


#### [▸ In-class outline](week-01.md)

----------------------------------------------------------------

## <a name="week2"></a>Week 2 (1/28): Provocations
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_2)
#### Coding, writing, and exercises
- Montfort, chp. 1 "Introduction"; "Installation and Setup" (for your information); chp. 1 "Modifying a Program"; chp. 2 "Calculating"
- “The Jupyter Notebook.” [http://jupyter-notebook.readthedocs.io/en/latest/notebook.html](http://jupyter-notebook.readthedocs.io/en/latest/notebook.html)
- Booth, Wayne C., et al., chp. 3 "From Topics to Questions". [*The Craft of Research*](https://utexas.instructure.com/courses/1216881/files/folder/FinalProject), Third Ed. University Of Chicago Press, 2008.
#### For discussion
- Borgman chp. 1 "Provocations" *Big Data, Little Data, No Data: Scholarship in the Networked World.* The MIT Press, 2015.
- Marche, Stephen. “Literature Is not Data: Against Digital Humanities.” *Los Angeles Review of Books*, October 28th, 2012.
                      [https://lareviewofbooks.org/essay/literature-is-not-data-against-digital-humanities](https://lareviewofbooks.org/essay/literature-is-not-data-against-digital-humanities)
- Read in order:
1. Manovich,  Lev.  2008. [“The Next Big Thing in Humanities, Arts, and Social Science Computing: Cultural Analytics”](https://www.hpcwire.com/2008/07/29/the_next_big_thing_in_humanities_arts_and_social_science_computing_cultural_analytics/). HPC Wire, July 29.
2. Manovich,  Lev. 2009. [“Cultural Analytics: Visualizing Cultural Patterns in the Era of ‘More Media.’""](http://manovich.net/content/04-projects/063-cultural-analytics-visualizing-cultural-patterns/60_article_2009.pdf) Software Studies Initiative [website](http://lab.softwarestudies.com/)).
3. Hall, Gary. “Toward a Postdigital Humanities: Cultural Analytics and the Computational Turn to Data-Driven Scholarship.” *American Literature* 85, no. 4 (January 1, 2013): 781–809.
- Padilla, T. ["On a Collections as Data Imperative."](http://digitalpreservation.gov/meetings/dcs16/tpadilla_OnaCollectionsasDataImperative_final.pdf).
#### Optional
- Kenner, Hugh. Sentences. *Harvard Book Review* No. 13/14 (Summer - Fall, 1989), pp. 3-4.
- Posner, Miriam. “Humanities Data: A Necessary Contradiction.” *Miriam Posner’s Blog*, June 25, 2015. [http://miriamposner.com/blog/humanities-data-a-necessary-contradiction](http://miriamposner.com/blog/humanities-data-a-necessary-contradiction)
- Gallinger, M. and Daniel Chudnov "Library of Congress Lab: Library of Congress Digital Scholars Lab Pilot Project Report."

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-02.md)

----------------------------------------------------------------

## <a name="week3"></a>Week 3 (2/5): Programming
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_3)
#### Coding, writing, and exercises
- Montfort, Chp. 3 "Double, Double"
- Allardice, Simon. “Foundations of Programming: Fundamentals, parts 1-3; part 5, just "part 5, Breaking your code apart"; and part 14, just “Python” and “Libraries and frameworks”. [http://www.lynda.com/JavaScript-tutorials/Foundations-of-Programming-Fundamentals/83603-2.html](http://www.lynda.com/JavaScript-tutorials/Foundations-of-Programming-Fundamentals/83603-2.html) [To access Lynda.com. follow links below, click “Log in,” then “Organizational Login,” and enter your UT EID and password.]
#### For discussion
- Introna, L. D. “The Enframing of Code: Agency, Originality and the Plagiarist.” *Theory, Culture & Society* 28, no. 6 (November 1, 2011): 113–41.
- Montfort “Why Program?” (p.267–77)
- Vee, Annette. "Sociomaterialities of Programming and Writing." Coding Literacy: How Computer Programming Is Changing Writing. The MIT Press, 2017.
- Shieber, Stuart M., [*Programming for Humanists*](http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf) pages 1–4, 2014. [http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf]


### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)


#### [▸ In-class outline](week-03.md)

----------------------------------------------------------------

## <a name="week4"></a>Week 4 (2/12): Data
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_4)
#### Coding, writing, and exercises
- Montfort chp 4. "Programming Fundamentals"; Montfort, chp. 5 "Standard Starting Points";
- Zhuang, Atima Han, Ishita Vedvyas, and Rishikesh Dole. “Tutorial: OpenRefine,” 2013. [http://casci.umd.edu/wp-content/uploads/2013/12/OpenRefine-tutorial-v1.5.pdf](http://casci.umd.edu/wp-content/uploads/2013/12/OpenRefine-tutorial-v1.5.pdf)
#### For discussion
- Borgman, chp 2 "What are Data?"
- Krumme, Coco. “What Data Doesn’t Do.” In *Beautiful Data: The Stories behind Elegant Data Solutions*, edited by Toby Segaran and Jeff Hammerbacher, 1st ed. Beijing ; Sebastopol, CA: O’Reilly, 2009.
- Rosenberg, "Data Before the Fact." In Gitelman, Lisa *"Raw Data" is an Oxymoron*. Cambridge: MIT Press, 2013.
#### Optional
- Borges, Luis. ["The Analytical Language of John Wilkins."](http://www.alamut.com/subj/artiface/language/johnWilkins.html)
- Nunberg, Geoffrey. "Google's Book Search: A Disaster for Scholars." *Chronicle of Higher Education.* 31 Aug. 2009.
- Fortune, Stephen. “A Brief History of Databases.” *Avant*, February 27th 2014. [https://web.archive.org/web/20150220031213/http://avant.org/media/history-of-databases](https://web.archive.org/web/20150220031213/http://avant.org/media/history-of-databases)
- Pechenick, Eitan Adam, et al. “Characterizing the Google Books Corpus: Strong Limits to Inferences of Socio-Cultural and Linguistic Evolution.” PLOS ONE, vol. 10, no. 10, Oct. 2015, p. e0137041.
- Zhang, Sarah. “The Pitfalls Of Using Google Ngram To Study Language.” *Wired.* 12 October 2015.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-04.md)
- OpenRefine


----------------------------------------------------------------


## <a name="week5"></a>Week 5 (2/19): Data Scholarship
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_5)
#### Coding, writing, and exercises
- Montfort chp. 6 "Text I" ([some hints on possible errors](https://github.com/tanyaclement/cpcda18.github.io/blob/master/montfort6-7.md))
- [“HTML Introduction”](http://www.w3schools.com/html/html_intro.asp) and [“HTML5 Introduction”](http://www.w3schools.com/html/html5_intro.asp), W3Schools.
#### For discussion
- Borgman chp. 3 "Data Scholarship"
- Liu. [“Drafts for Against the Cultural Singularity”](http://liu.english.ucsb.edu/drafts-for-against-the-cultural-singularity/) Alan Liu. 2 May 2016.
- Read in order:
1. Winner, Langdon. “Do Artifacts Have Politics?” *Daedalus* 109, no. 1 (1980): 121–36.
2. Joerges, B. “Do Politics Have Artefacts?” *Social Studies of Science* 29, no. 3 (June 1, 1999): 411–31.
3. Sacasas, Michael. “Do Artifacts Have Ethics?” *The Frailest Thing*, November 29, 2014. [http://thefrailestthing.com/2014/11/29/do-artifacts-have-ethics](http://thefrailestthing.com/2014/11/29/do-artifacts-have-ethics/)

### Assignment
[REQUIRED Discussion post, 4 points](https://utexas.instructure.com/courses/1216881/discussion_topics)

### Speaker: Maria Fernandez

#### [▸ In-class outline](week-05.md)

----------------------------------------------------------------


## <a name="week6"></a>Week 6 (2/26): Data Set Reviews
In class presentations of Data Set Reviews

### Assignment
[Data Set Review](https://utexas.instructure.com/courses/1216881/assignments/4249399)

#### [▸ In-class outline](week-06.md)
- Downloading with Wget
- Fetching and Parsing Data from the Web with OpenRefine

----------------------------------------------------------------
# II. Interpretive Framing with Data
## <a name="week7"></a>Week 7 (3/5): Audience
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_7)
#### Coding, writing, and exercises
- Montfort chp. 7 "Text II" ([some hints on possible errors](https://github.com/tanyaclement/cpcda18.github.io/blob/master/montfort6-7.md))
#### For discussion
- Borgman chp. 4 "Data Diversity"
- Hitchcock, Tim. “Digital Searching and the Re-formulation of Historical Knowledge” 2008. In *The Virtual Representation of the Past*, edited by Mark Greenglass and Lorna Hughes, 81-90. Ashgate: 2008.
- Piper, A. Think Small: On Literary Modeling. *PMLA*, Volume 132, Number 3, May 2017, pp. 651–658.
- Pound, Scott. “Kenneth Goldsmith and the Poetics of Information.” PMLA, vol. 130, no. 2, Mar. 2015, pp. 315–30.
### Optional
- Neff, Gina, Tanweer, Anissa, Fiore-Gartland, Brittany, Osburn, Laura  Critique and Contribute: A Practice-Based Framework for Improving Critical Data Studies and Data Science. *Big Data* 5, no. 2, 2017.
- Oualline, Steve. [“The End of Line Puzzle.” The Practical Programmer.](http://www.oualline.com/practical.programmer/eol.html)

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)
<!--
Add Montfort Text II exercise into a discussion post pg. 145.
-->

#### [▸ In-class outline](week-07.md)
- Getting Files
- Revisiting the basics

----------------------------------------------------------------
# SPRING BREAK (3/12)
----------------------------------------------------------------

## <a name="week8"></a>Week 8 (3/19): Open Access
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_8)
#### Coding, writing, and exercises
- Montfort chp. 8 "Image I"
- Albon, Chris. “String Operations.” [http://chrisalbon.com/python/string_operations.html](https://chrisalbon.com/python/basics/string_operations/)
#### For discussion
- Christen, Kim. “Does Information Really Want to be Free? Indigenous Knowledge Systems and the Question of Openness.” *International Journal of Communication* 6 (2012), 2870–2893.
- Day, Ronald E. “Governing Expression: Social Big Data and Neoliberalism.” In *Indexing It All: The Subject in the Age of Documentation*, Information, and Data, 123–44. History and Foundations of Information Science. Cambridge, Massachusetts: The MIT Press, 2014.
- Pomerantz, Jeffrey. “The Future of Metadata.” In *Metadata*. The MIT Press Essential Knowledge Series. Cambridge, MA ; London, England: The MIT Press, 2015.
### Optional
- Peters, Justin. *The Idealist: Aaron Swartz and the Rise of Free Culture on the Internet*, Chapters 7 and 8. New York: Scribner, 2016.
- O’Sullivan, Michael. “Aaron Swartz, New Technologies, and the Myth of Open Access.” In *Academic Barbarism, Universities and Inequality*. Palgrave Critical University Studies. Houndmills, Basingstoke, Hampshire ; New York, NY: Palgrave Macmillan, 2016.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

### Speaker: Maria Fernandez

#### [▸ In-class outline](week-08.md)
- CSV Input/Output in Python

----------------------------------------------------------------
## <a name="week9"></a>Week 9 (3/26): Data Modeling

### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_9)
#### For discussion
- Kreiss, D., M. Finn, and F. Turner. “The Limits of Peer Production: Some Reminders from Max Weber for the Network Society.” New Media & Society 13, no. 2 (March 1, 2011): 243–59.
- Swartz, Aaron. “Building a Platform: Providing APIs.” In *Aaron Swartz’s ‘A Programmable Web’: An Unfinished Work*, 31–39. San Rafael, CA: Morgan & Claypool Publishers, 2013.
- van Hooland, Seth, and Ruben Verborgh. “Modelling.” In *Linked Data for Libraries, Archives and Museums: How to Clean, Link and Publish Your Metadata*, 11–70. Chicago: Neal-Schuman, 2014.
- Kelly, Chelsea Emelie. [“Beyond Digital: Open Collections & Cultural Institutions,”](https://artmuseumteaching.com/2014/11/06/beyond-digital-open-collections-cultural-institutions) 2014.
#### Optional
- Manzo, Christina, Geoff Kaufman, Sukdith Punjasthitkul, and Mary Flanagan. “‘By the People, For the People’: Assessing the Value of Crowdsourced, User-Generated Metadata.” *Digital Humanities Quarterly* 9, no. 1 (2015). [http://www.digitalhumanities.org/dhq/vol/9/1/000204/000204.html](http://www.digitalhumanities.org/dhq/vol/9/1/000204/000204.html)
- Veltman, Noah. [Web APIs for non-programmers](https://schoolofdata.org/2013/11/18/web-apis-for-non-programmers/). November 18, 2013. *School of Data*.

### Assignment
[*Proposal due Friday, March 23 at 11:59pm; Peer reviews due by class March 26 at 3pm*](https://utexas.instructure.com/courses/1216881/assignments/4166696)

#### [▸ In-class outline](week-09.md)
- Using the Google Books REST API
- New York Times article scrape
- Scraping and Parsing XML
- Fetching and Parsing Data from the Web with OpenRefine, APIs

----------------------------------------------------------------


## <a name="week10"></a>Week 10 (4/2): Theory
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_10)
#### Coding, writing, and exercises
- Montfort chp. 10 "Text III"
- Final project directory: Booth chp. 4 "From Questions to a Problem"
#### For discussion
- Conley, Tara L. "Decoding Black Feminist Hashtags as Becoming" The Black Scholar Vol. 47 , Iss. 3, 2017.
- Klein, Lauren. ["Distant Reading after Moretti"](http://lklein.com/2018/01/distant-reading-after-moretti/). MLA Conference, January 2018.
- Ramsay, Stephen. “Chapter 1: An Algorithmic Criticism.” In *Reading Machines: Toward an Algorithmic Criticism*, 1–17. Topics in the Digital Humanities. Urbana: University of Illinois Press, 2011.
- Underwood, T. ["Theorizing Research Practices We Forgot to Theorize Twenty Years Ago"](https://www.ideals.illinois.edu/bitstream/handle/2142/48906/theorizing.pdf?sequence=2). *Representations*, Vol. 127 No. 1, Summer 2014; (pp. 64-72).
#### Optional
- Risam, R. ["Beyond the Margins: Intersectionality and the Digital Humanities"](http://www.digitalhumanities.org/dhq/vol/9/2/000208/000208.html) *Digital Humanities Quarterly*, Vol. 9 No. 2, 2015.
- Presner, Todd. ["Critical Theory and the Mangle of Digital Humanities"](http://www.toddpresner.com/wp-content/uploads/2012/09/Presner_2012_DH_FINAL.pdf)[draft version; 2012)

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-10.md)
- Unsupervised learning: Latent Dirichlet allocation (LDA) topic modeling
- Supervised learning: Naive Bayes classification
- Fetching and Parsing Data from the Web with OpenRefine, Advanced APIs
----------------------------------------------------------------

## <a name="week11"></a>Week 11 (4/9): Methods
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_11)
#### Coding, writing, and exercises

- “Working With Text Data.” scikit-learn. [http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html](http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html)
- Khan, Khairullah, Baharudin, Baharum, Lam Hong Lee. “A Review of Machine Learning Algorithms for Text-Documents Classification.” *Journal of Advances in Information Technology* 1, no. 1 (February 1, 2010).
- Wolfram, S. Machine Learning for Middle Schoolers. Stephen Wolfram Blog. 11 May 2017. [http://blog.stephenwolfram.com/2017/05/machine-learning-for-middle-schoolers/#comments](http://blog.stephenwolfram.com/2017/05/machine-learning-for-middle-schoolers/#comments)
#### For discussion
- Griffiths, Devin. "The Comparative Method and the History of the Modern Humanities" *History of Humanities*, Volume 2, Number 2, 2017.
- Moretti, F. ["Conjectures in World Literature"](https://newleftreview.org/II/1/franco-moretti-conjectures-on-world-literature) *New Left Review* 1, January-February 2000.
- Seaver, Nick ["Algorithms as culture: Some tactics for the ethnography of algorithmic systems"](http://journals.sagepub.com/doi/10.1177/2053951717738104) Big Data and Society. 9 Nov. 2017
- Underwood, Ted. ["A Genealogy of Distant Reading"](http://www.digitalhumanities.org/dhq/vol/11/2/000317/000317.html). *Digital Humanities Quarterly* Volume 11, Number 2, 2017.
#### Optional
- Borgman chp. 7
- Berendt, Bettina, Preibusch, Soren. Toward Accountable Discrimination-Aware Data Mining: The Importance of Keeping the Human in the Loop—and Under the Looking Glass. *Big Data*. Volume 5, Number 2, 2017.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

### Speaker: Maria Fernandez
#### [▸ In-class outline](week-11.md)
- Supervised learning with multiple classifiers: Naive Bayes, k-nearest neighbor, Logistic Regression, Support Vector Machine (SVM), Multi-layer perceptron classifier

----------------------------------------------------------------

## <a name="week12"></a>Week 12 (4/16): Statistics and Visualization
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_12)
#### Coding, writing, and exercises
- Montfort chp. 11 “Statistics and Visualization.”
- Brew, Chris. “Language Processing: Statistical Methods.” In *Encyclopedia of Language & Linguistics*, edited by Keith Brown, 2nd ed., 12:597–604. Elsevier, 2006.
- Gries, Stefan. [“Useful statistics for corpus linguistics.”](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.160.9846&rep=rep1&type=pdf).
- McCandles, David. [*Information is Beautiful*](http://www.informationisbeautiful.net).
- Norvig, Peter. “Natural Language Corpus Data.” In *Beautiful Data: The Stories Behind Elegant Data Solutions*, edited by Toby Segaran and Jeff Hammerbacher, 1st ed. Beijing ; Sebastopol, CA: O’Reilly, 2009.
#### For discussion
- Burrows, John. [“Textual Analysis.”](http://digitalhumanities.org/companion/view?docId=blackwell/9781405103213/9781405103213.xml&doc.view=print&chunk.id=ss1-4-4&toc.depth=1&toc.id=0) In Companion to Digital Humanities, edited by Susan Schreibman, Ray Siemens, and John Unsworth.
- Catherine D’Ignazio and Lauren F. Klein, [“Feminist Data Visualization”](http://www.kanarinka.com/wp-content/uploads/2015/07/IEEE_Feminist_Data_Visualization.pdf) IEEE VIS Conference, Baltimore, October, 23-28, 2016. 7, 2016
- Lev Manovich. ["Cultural Data Possibilities and limitations of the digital data universe"](http://manovich.net/content/04-projects/102-cultural-data/cultural_data_article.pdf). Oliver Grau, ed., with Wendy Coones and Viola Rühse, Museum and Archive on the Move. Changing Cultural Institutions in the Digital Era (Berlin, Boston: De Gruyter, 2017), 259-276.
- Stack, John. ["Exploring museum collections online: Some background reading'](https://lab.sciencemuseum.org.uk/exploring-museum-collections-online-some-background-reading-da5a332fa2f8). *Science Museum Group Digital Lab* January 23, 2018.
- Thompson, Clive. [“The Surprising History of the Infographic.”](http://www.smithsonianmag.com/history/surprising-history-infographic-180959563/?no-ist)
#### Optional
- Moretti, Franco. “Graphs.” In *Graphs, Maps, Trees: Abstract Models for Literary History*, 3–33. London ; New York: Verso, 2007.
- Ramsay, Stephen. “Chapter 3: Potential Readings.” In *Reading Machines: Toward an Algorithmic Criticism*, 33–57. Topics in the Digital Humanities. Urbana: University of Illinois Press, 2011.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-12.md)
- Tableau
----------------------------------------------------------------

## <a name="week13"></a>Week 13 (4/23): Features
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_13)
#### Coding, writing, and exercises
- Kazil, Jacqueline, and Katharine Jarmul. “PDFs and Problem Solving in Python.” In *Data Wrangling with Python: Tips and Tools to Make Your Life Easier*, 91–126. O’Reilly, 2016.
- Albon, Chris. “Parse JSON File.” [http://chrisalbon.com/python/json_parse_file.html](https://github.com/chrisalbon/code_py/blob/master/json_parse_file.ipynb)
- Lundh, Fredrik. “Elements and Element Trees.” [http://effbot.org/zone/element.htm](http://effbot.org/zone/element.htm) [Python XML tutorial]
- Beazley, David, and Brian K. Jones. “Chapter 6: Data Encoding and Processing.” In Python Cookbook: *recipes for Mastering Python 3*, 3. ed., 175–216. Bejing: O’Reilly, 2013.
#### For discussion
- Brown and Mandell, ["The Identity Issue: An Introduction."](http://culturalanalytics.org/2018/02/the-identity-issue-an-introduction/) *Journal of Cultural Analytics* 13 February 2018.
- Hammond, Adam. "The double bind of validation: distant reading and the digital humanities' 'trough of disillusionment." *Literature Compass* 14, no. 8 (August 1, 2017): no. pg.
- Schmidt, B. ["Do Digital Humanists Need to Understand Algorithms?"](http://dhdebates.gc.cuny.edu/debates/text/99).
- Witmore, Michael. 2016. “Latour, the Digital Humanities, and the Divided Kingdom of Knowledge.” *New Literary History* 47 (2): 353–75.
#### Have some fun!
- Scroll through [these examples of neural networks inventing things based on example](http://aiweirdness.com/) such as insect names, thesis titles, guinea pig names, and pie
- “Transparency” through end-user parameter modification or [Change your algorithm for what Spotify picks for you](https://www.theverge.com/tldr/2018/2/5/16974194/spotify-recommendation-algorithm-playlist-hack-nelson)
#### Optional
- Clement, T. and McLaughlin, S. [“Measured Applause: Toward a Cultural Analysis of Audio Collections.”](http://culturalanalytics.org/2016/05/measured-applause-toward-a-cultural-analysis-of-audio-collections/) *Cultural Analytics*, vol. 1, no. 1, 2016.
- Liu, Alan. “The Meaning of the Digital Humanities.” *PMLA* 128, no. 2 (March 2013): 409–23.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-13.md)


----------------------------------------------------------------

## <a name="week14"></a>Week 14 (4/30): Final Presentations

[Final Presentation due](https://utexas.instructure.com/courses/1216881/assignments/4166564)

5/7: [Final Project due](https://utexas.instructure.com/courses/1216881/assignments/4166548)

----------------------------------------------------------------
## Additional resources:
### Programming tutorials
**[Installation Tutorials](tutorials/)**
- [Jeroen Janssens Seven Command Line Tools for Data Science (2013) workbench.](https://hub.docker.com/r/wlanderson/dsatclwb/)
- Karsdorp, Folgert. [Python Programming for the Humanities](http://www.karsdorp.io/python-course/)
- Marini, Joe. [“Up and Running with Python.”](http://www.lynda.com/Python-tutorials/Welcome/122467/142550-4.html) Lynda.com.
- Shieber, Stuart M., [*Programming for Humanists*](http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf) pages 1–4, 2014. [http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf]
- Williamson, Evan Peter. [Fetching and Parsing Data from the Web with OpenRefine](https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine#start-sonnets-project)
### Readings
- Code of Best Practices in Fair Use for Academic and Research Libraries*. Association of Research Libraries, 2012*. [http://www.arl.org/storage/documents/publications/code-of-best-practices-fair-use.pdf](http://www.arl.org/storage/documents/publications/code-of-best-practices-fair-use.pdf)
- “The Digital Public Library of America Policy Statement on Metadata,” 2013. [http://dp.la/info/wp-content/uploads/2013/04/DPLAMetadataPolicy.pdf](http://dp.la/info/wp-content/uploads/2013/04/DPLAMetadataPolicy.pdf)
- “Creative Commons: About the Licenses.” [https://creativecommons.org/licenses/](https://creativecommons.org/licenses/)
- DRM article: [http://infojustice.org/wp-content/uploads/2015/03/band03102015.pdf](http://infojustice.org/wp-content/uploads/2015/03/band03102015.pdf)
- Juola, P. and Ramsay, S. [Six Septembers: Mathematics for the Humanist](http://digitalcommons.unl.edu/zeabook/55/). Zea E-Books.
- American Civil Liberties Union. ["First Amendment Lawsuit Brought on Behalf of Academic Researchers and Journalists Who Fear Prosecution Under the Computer Fraud and Abuse Act."](https://www.aclu.org/news/aclu-challenges-law-preventing-studies-big-data-discrimination)
- Sanger, David E., and Eric Schmitt. “Snowden Used Low-Cost Tool to Best N.S.A.” The New York Times. February 8, 2014. [http://www.nytimes.com/2014/02/09/us/snowden-used-low-cost-tool-to-best-nsa.html](http://www.nytimes.com/2014/02/09/us/snowden-used-low-cost-tool-to-best-nsa.html)
- Sims, Nancy. [“Library Licensing and Criminal Law: The Aaron Swartz Case.”](http://crln.acrl.org/index.php/crlnews/article/view/8637/9062) *College & Research Libraries News* 72, no. 9 (2011): 534–37.
- [Python tutorials](https://www.programiz.com/python-programming#tutorial) at [Programiz](https://www.programiz.com/).
