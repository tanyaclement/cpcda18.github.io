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

Montfort, Nick. Exploratory Programming for the Arts and Humanities. Cambridge, MA: The MIT Press, 2016.

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

- Bod, Rens. "Introduction: the Quest for Principles and Patterns." A New History of the Humanities: The Search for Principles and Patterns from Antiquity to the Present. Oxford University Press, 2013, pp. 1 - 12. *Note: You must be logged in as a UT student to retrieve this text*: [http://catalog.lib.utexas.edu/record=b8902003~S29](http://catalog.lib.utexas.edu/record=b8902003~S29)


#### [▸ In-class outline](week-01.md)

----------------------------------------------------------------

## <a name="week2"></a>Week 2 (1/28): Provocations
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_2)
#### Coding, writing, and exercises
- Montfort, chp. 1 "Introduction"; "Installation and Setup" (for your information); chp. 2 "Calculating"
- “The Jupyter Notebook.” [http://jupyter-notebook.readthedocs.io/en/latest/notebook.html](http://jupyter-notebook.readthedocs.io/en/latest/notebook.html)
- [Booth][https://utexas.instructure.com/courses/1216881/files/folder/FinalProject], chp. 3 "From Topics to Questions".
#### For discussion
- Borgman chp. 1 "Provocations"
- Read in order:
1. Manovich,  Lev.  2008. [“The Next Big Thing in Humanities, Arts, and Social Science Computing: Cultural Analytics”](https://www.hpcwire.com/2008/07/29/the_next_big_thing_in_humanities_arts_and_social_science_computing_cultural_analytics/). HPC Wire, July 29.
2. Manovich,  Lev. 2009. [“Cultural Analytics: Visualizing Cultural Patterns in the Era of ‘More Media.’""](http://manovich.net/content/04-projects/063-cultural-analytics-visualizing-cultural-patterns/60_article_2009.pdf) Software Studies Initiative [website](http://lab.softwarestudies.com/)).
3. Hall, Gary. “Toward a Postdigital Humanities: Cultural Analytics and the Computational Turn to Data-Driven Scholarship.” *American Literature* 85, no. 4 (January 1, 2013): 781–809.
- Marche, Stephen. “Literature Is not Data: Against Digital Humanities.” *Los Angeles Review of Books*, October 28th, 2012.
                      [https://lareviewofbooks.org/essay/literature-is-not-data-against-digital-humanities](https://lareviewofbooks.org/essay/literature-is-not-data-against-digital-humanities)
- Padilla, T. ["On a Collections as Data Imperative."](http://digitalpreservation.gov/meetings/dcs16/tpadilla_OnaCollectionsasDataImperative_final.pdf).

#### Optional
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

<!--
### Optional

-   Shieber, Stuart M., *Programming for Humanists* pages 1–28, 2014. [http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf](http://blogs.harvard.edu/programmingforhumanists/files/2014/12/proghum.pdf)


-   Stephenson, Neal. “In the Beginning Was the Command Line.” Cryptonomicon, 1999. <http://www.cryptonomicon.com/beginning.html>. [TXT](http://www.cryptonomicon.com/command.zip).


-  Marini, Joe. “Up and Running with Python.” Lynda.com.
            [http://www.lynda.com/Python-tutorials/Welcome/122467/142550-4.html](http://www.lynda.com/Python-tutorials/Welcome/122467/142550-4.html)
-->

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)


#### [▸ In-class outline](week-03.md)


----------------------------------------------------------------

## <a name="week4"></a>Week 4 (2/12): Data

### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_4)
#### Coding, writing, and exercises
- Montfort chp 4. "Programming Fundamentals"; Montfort, chp. 5 "Standard Starting Points";
#### For discussion
- Borgman, chp 2 "What are Data?" *Big Data, Little Data, No Data: Scholarship in the Networked World.* The MIT Press, 2015.
- Fortune, Stephen. “A Brief History of Databases.” *Avant*, February 27th 2014. [https://web.archive.org/web/20150220031213/http://avant.org/media/history-of-databases](https://web.archive.org/web/20150220031213/http://avant.org/media/history-of-databases)
- Krumme, Coco. “What Data Doesn’t Do.” In *Beautiful Data: The Stories behind Elegant Data Solutions*, edited by Toby Segaran and Jeff Hammerbacher, 1st ed. Beijing ; Sebastopol, CA: O’Reilly, 2009.
- Rosenthal, "Data Before the Fact." In Gitelman, Lisa *"Raw Data" is an Oxymoron*. Cambridge: MIT Press, 2013.
### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-04.md)


----------------------------------------------------------------


## <a name="week5"></a>Week 5 (2/19): Scholarship
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_5)
#### For discussion
- Borgman chp. 3 "Data Scholarship"
- Read in order:
1. Winner, Langdon. “Do Artifacts Have Politics?” *Daedalus* 109, no. 1 (1980): 121–36.
2. Joerges, B. “Do Politics Have Artefacts?” *Social Studies of Science* 29, no. 3 (June 1, 1999): 411–31.
3. Sacasas, Michael. “Do Artifacts Have Ethics?” *The Frailest Thing*, November 29, 2014. [http://thefrailestthing.com/2014/11/29/do-artifacts-have-ethics](http://thefrailestthing.com/2014/11/29/do-artifacts-have-ethics/)
- Liu. [“Drafts for Against the Cultural Singularity”](http://liu.english.ucsb.edu/drafts-for-against-the-cultural-singularity/) Alan Liu. 2 May 2016.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)


----------------------------------------------------------------


## <a name="week6"></a>Week 6 (2/26): Data Set Reviews
In class presentations of Data Set Reviews

### Assignment
[Data Set Review](https://utexas.instructure.com/courses/1216881/assignments/4249399)

----------------------------------------------------------------
# II. Interpretive Framing with Data
## <a name="week7"></a>Week 7 (3/5): Audience

### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_7)
#### Coding, writing, and exercises
- Montfort chp. 6 "Text I"
- Albon, Chris. “String Operations.” [http://chrisalbon.com/python/string_operations.html](http://chrisalbon.com/python/string_operations.html)
- [“HTML Introduction”](http://www.w3schools.com/html/html_intro.asp) and [“HTML5 Introduction”](http://www.w3schools.com/html/html5_intro.asp), W3Schools.

#### For discussion
- Hitchcock, Tim. “Digital Searching and the Re-formulation of Historical Knowledge” 2008. In *The Virtual Representation of the Past*, edited by Mark Greenglass and Lorna Hughes, 81-90. Ashgate: 2008.
- Liu, Alan. “The Meaning of the Digital Humanities.” *PMLA* 128, no. 2 (March 2013): 409–23.
- Pound, Scott. “Kenneth Goldsmith and the Poetics of Information.” PMLA, vol. 130, no. 2, Mar. 2015, pp. 315–30.
- Neff, Gina, Tanweer, Anissa, Fiore-Gartland, Brittany, Osburn, Laura  Critique and Contribute: A Practice-Based Framework for Improving Critical Data Studies and Data Science. *Big Data* 5, no. 2, 2017.
### Optional Readings
- Greenwald, Glenn. “Chapter 1: Contact.” In *No Place to Hide: Edward Snowden, the NSA, and the U.S. Surveillance State*, 2015.
- American Civil Liberties Union. "First Amendment Lawsuit Brought on Behalf of Academic Researchers and Journalists Who Fear Prosecution Under the Computer Fraud and Abuse Act." [https://www.aclu.org/news/aclu-challenges-law-preventing-studies-big-data-discrimination](https://www.aclu.org/news/aclu-challenges-law-preventing-studies-big-data-discrimination)

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-07.md)

----------------------------------------------------------------
# SPRING BREAK (3/12)

## <a name="week8"></a>Week 8 (3/19): Data Models
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_8)
#### Coding, writing, and exercises
- Montfort chp. 7 "Text II"
- Zhuang, Atima Han, Ishita Vedvyas, and Rishikesh Dole. “Tutorial: OpenRefine,” 2013. [http://casci.umd.edu/wp-content/uploads/2013/12/OpenRefine-tutorial-v1.5.pdf](http://casci.umd.edu/wp-content/uploads/2013/12/OpenRefine-tutorial-v1.5.pdf)
#### For discussion
- Borgman chp. 4 "Data Diversity"
- van Hooland, Seth, and Ruben Verborgh. “Modelling.” In *Linked Data for Libraries, Archives and Museums: How to Clean, Link and Publish Your Metadata*, 11–70. Chicago: Neal-Schuman, 2014.
- Swartz, Aaron. “Building a Platform: Providing APIs.” In *Aaron Swartz’s ‘A Programmable Web’: An Unfinished Work*, 31–39. San Rafael, CA: Morgan & Claypool Publishers, 2013.
### Optional Readings
-   Code of Best Practices in Fair Use for Academic and Research Libraries*. Association of Research Libraries, 2012*. [http://www.arl.org/storage/documents/publications/code-of-best-practices-fair-use.pdf](http://www.arl.org/storage/documents/publications/code-of-best-practices-fair-use.pdf)
-   “The Digital Public Library of America Policy Statement on Metadata,” 2013. [http://dp.la/info/wp-content/uploads/2013/04/DPLAMetadataPolicy.pdf](http://dp.la/info/wp-content/uploads/2013/04/DPLAMetadataPolicy.pdf)
-   “Creative Commons: About the Licenses.” [https://creativecommons.org/licenses/](https://creativecommons.org/licenses/)
-   DRM article: [http://infojustice.org/wp-content/uploads/2015/03/band03102015.pdf](http://infojustice.org/wp-content/uploads/2015/03/band03102015.pdf)
- Manzo, Christina, Geoff Kaufman, Sukdith Punjasthitkul, and Mary Flanagan. “‘By the People, For the People’: Assessing the Value of Crowdsourced, User-Generated Metadata.” *Digital Humanities Quarterly* 9, no. 1 (2015). [http://www.digitalhumanities.org/dhq/vol/9/1/000204/000204.html](http://www.digitalhumanities.org/dhq/vol/9/1/000204/000204.html)
- Pomerantz, Jeffrey. “The Future of Metadata.” In *Metadata*. The MIT Press Essential Knowledge Series. Cambridge, MA ; London, England: The MIT Press, 2015.
### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-08.md)

----------------------------------------------------------------
## <a name="week9"></a>Week 9 (3/26): Open Access

### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_9)
#### Coding, writing, and exercises
- Montfort chp. 8 "Image I"
#### For discussion
- Christen, Kim. “Does Information Really Want to be Free? Indigenous Knowledge Systems and the Question of Openness.” International Journal of Communication 6 (2012), 2870–2893.
- Peters, Justin. *The Idealist: Aaron Swartz and the Rise of Free Culture on the Internet*, Chapters 7 and 8. New York: Scribner, 2016.
- O’Sullivan, Michael. “Aaron Swartz, New Technologies, and the Myth of Open Access.” In *Academic Barbarism, Universities and Inequality*. Palgrave Critical University Studies. Houndmills, Basingstoke, Hampshire ; New York, NY: Palgrave Macmillan, 2016.
- Kelly, Chelsea Emelie. “Beyond Digital: Open Collections & Cultural Institutions,” 2014.  [https://artmuseumteaching.com/2014/11/06/beyond-digital-open-collections-cultural-institutions](https://artmuseumteaching.com/2014/11/06/beyond-digital-open-collections-cultural-institutions)

### Optional Readings
- Sims, Nancy. “Library Licensing and Criminal Law: The Aaron Swartz Case.” *College & Research Libraries News* 72, no. 9 (2011): 534–37. [http://crln.acrl.org/content/72/9/534.short](http://crln.acrl.org/content/72/9/534.short).
- Day, Ronald E. “Governing Expression: Social Big Data and Neoliberalism.” In *Indexing It All: The Subject in the Age of Documentation*, Information, and Data, 123–44. History and Foundations of Information Science. Cambridge, Massachusetts: The MIT Press, 2014.
- Sanger, David E., and Eric Schmitt. “Snowden Used Low-Cost Tool to Best N.S.A.” The New York Times. February 8, 2014. [http://www.nytimes.com/2014/02/09/us/snowden-used-low-cost-tool-to-best-nsa.html](http://www.nytimes.com/2014/02/09/us/snowden-used-low-cost-tool-to-best-nsa.html)

### Assignment
[Due: Proposal](https://utexas.instructure.com/courses/1216881/assignments/4166696)

#### [▸ In-class outline](week-09.md)


----------------------------------------------------------------


## <a name="week10"></a>Week 10 (4/2): Theory
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_10)
#### Coding, writing, and exercises
- Montfort chp. 9 "Image II"
- Final project directory: Booth chp. 4 "From Questions to a Problem"
#### For discussion
- Klein, Lauren. ["Distant Reading after Moretti"](http://lklein.com/2018/01/distant-reading-after-moretti/). MLA Conference, January 2018.
- Ramsay, Stephen. “Chapter 1: An Algorithmic Criticism.” In *Reading Machines: Toward an Algorithmic Criticism*, 1–17. Topics in the Digital Humanities. Urbana: University of Illinois Press, 2011.
- Freelon, Deen Goodwin, Charlton D. McIlwain, and Meredith D. Clark. “Beyond the Hashtags: #Ferguson, #Blacklivesmatter, and the Online Struggle for Offline Justice,” 2016. [http://cmsimpact.org/wp-content/uploads/2016/03/beyond_the_hashtags_2016.pdf](http://cmsimpact.org/wp-content/uploads/2016/03/beyond_the_hashtags_2016.pdf)

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-10.md)

----------------------------------------------------------------

## <a name="week11"></a>Week 11 (4/9): Methods
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_11)
#### Coding, writing, and exercises
- Montfort chp. 10 "Text III"
- Kazil, Jacqueline, and Katharine Jarmul. “PDFs and Problem Solving in Python.” In *Data Wrangling with Python: Tips and Tools to Make Your Life Easier*, 91–126. O’Reilly, 2016.
- Albon, Chris. “Parse JSON File.” [http://chrisalbon.com/python/json_parse_file.html](https://github.com/chrisalbon/code_py/blob/master/json_parse_file.ipynb)
- Lundh, Fredrik. “Elements and Element Trees.” [http://effbot.org/zone/element.htm](http://effbot.org/zone/element.htm) [Python XML tutorial]
- Beazley, David, and Brian K. Jones. “Chapter 6: Data Encoding and Processing.” In Python Cookbook: *recipes for Mastering Python 3*, 3. ed., 175–216. Bejing: O’Reilly, 2013.
- “Working With Text Data.” scikit-learn. [http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html](http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html)
- Baharudin, Baharum, Lam Hong Lee, and Khairullah Khan. “A Review of Machine Learning Algorithms for Text-Documents Classification.” *Journal of Advances in Information Technology* 1, no. 1 (February 1, 2010).
- Wolfram, S. Machine Learning for Middle Schoolers. Stephen Wolfram Blog. 11 May 2017. [http://blog.stephenwolfram.com/2017/05/machine-learning-for-middle-schoolers/#comments](http://blog.stephenwolfram.com/2017/05/machine-learning-for-middle-schoolers/#comments)
- Norvig, Peter. “Natural Language Corpus Data.” In *Beautiful Data: The Stories Behind Elegant Data Solutions*, edited by Toby Segaran and Jeff Hammerbacher, 1st ed. Beijing ; Sebastopol, CA: O’Reilly, 2009.
#### For discussion
- Schmidt, B. "Do Digital Humanists Need to Understand Algorithms? <http://dhdebates.gc.cuny.edu/debates/text/99>
- Witmore, Michael. 2016. “Latour, the Digital Humanities, and the Divided Kingdom of Knowledge.” New Literary History 47 (2): 353–75.
“Textual Analysis.”
- Underwood, Ted. A Genealogy of Distant Reading *Digital Humanities Quarterly* Volume 11, Number 2, 2017.

### Optional Reading
- Julia Angwin, Jeff Larson, Surya Mattu and Lauren Kirchner, ProPublica. “Machine Bias.” *ProPublica*. May 23, 2016. [https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)
- Berendt, Bettina, Preibusch, Soren. Toward Accountable Discrimination-Aware Data Mining: The Importance of Keeping the Human in the Loop—and Under the Looking Glass.Big DataVolume 5, Number 2, 2017.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-11.md)


----------------------------------------------------------------

## <a name="week12"></a>Week 12 (4/16): Statistics and Visualization
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_12)
#### Coding, writing, and exercises
- Montfort chp. 11 “Statistics and Visualization.”
- Brew, Chris. “Language Processing: Statistical Methods.” In Encyclopedia of Language & Linguistics, edited by Keith Brown, 2nd ed., 12:597–604. Elsevier, 2006.
- Gries, Stefan. “Useful statistics for corpus linguistics.” <http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.160.9846&rep=rep1&type=pdf>
- McCandles, David. *Information is Beautiful*. *http://www.informationisbeautiful.net*
#### For discussion
- Burrows, John. [“Textual Analysis.”](http://digitalhumanities.org/companion/view?docId=blackwell/9781405103213/9781405103213.xml&doc.view=print&chunk.id=ss1-4-4&toc.depth=1&toc.id=0) In Companion to Digital Humanities, edited by Susan Schreibman, Ray Siemens, and John Unsworth.
- Catherine D’Ignazio and Lauren F. Klein, [“Feminist Data Visualization”](http://www.kanarinka.com/wp-content/uploads/2015/07/IEEE_Feminist_Data_Visualization.pdf) IEEE VIS Conference, Baltimore, October, 23-28, 2016. 7, 2016
- Lev Manovich. ["Cultural Data Possibilities and limitations of the digital data universe"](http://manovich.net/content/04-projects/102-cultural-data/cultural_data_article.pdf). Oliver Grau, ed., with Wendy Coones and Viola Rühse, Museum and Archive on the Move. Changing Cultural Institutions in the Digital Era (Berlin, Boston: De Gruyter, 2017), 259-276.
- Underwood, T. ["Theorizing Research Practices We Forgot to Theorize Twenty Years Ago"](https://www.ideals.illinois.edu/bitstream/handle/2142/48906/theorizing.pdf?sequence=2). *Representations*, Vol. 127 No. 1, Summer 2014; (pp. 64-72). or GEANEALOGY?
### Optional Readings
- Thompson, Clive. “The Surprising History of the Infographic.” <http://www.smithsonianmag.com/history/surprising-history-infographic-180959563/?no-ist>
- Manovich, Lev. “What Is Visualisation?” *Visual Studies* 26, no. 1 (March 15, 2011): 36–49. <http://www.tandfonline.com/doi/abs/10.1080/1472586X.2011.548488>.
- Moretti, Franco. “Graphs.” In *Graphs, Maps, Trees: Abstract Models for Literary History*, 3–33. London ; New York: Verso, 2007.
- Ramsay, Stephen. “Chapter 3: Potential Readings.” In *Reading Machines: Toward an Algorithmic Criticism*, 33–57. Topics in the Digital Humanities. Urbana: University of Illinois Press, 2011.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-13.md)

----------------------------------------------------------------

## <a name="week13"></a>Week 13 (4/23): Features
### Readings
- [Readings in Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_13)
#### Coding, writing, and exercises
**[Canvas](https://utexas.instructure.com/courses/1216881/files/folder/Week_12)**
#### For discussion
- Clement, T. and McLaughlin, S. “Measured Applause: Toward a Cultural Analysis of Audio Collections.” Cultural Analytics, vol. 1, no. 1, 2016. [http://culturalanalytics.org/2016/05/measured-applause-toward-a-cultural-analysis-of-audio-collections/](http://culturalanalytics.org/2016/05/measured-applause-toward-a-cultural-analysis-of-audio-collections/)
- Seaver, Nick ["Algorithms as culture: Some tactics for the ethnography of algorithmic systems"](http://journals.sagepub.com/doi/10.1177/2053951717738104) Big Data and Society. 9 Nov. 2017
- Hammond, Adam. "The double bind of validation: distant reading and the digital humanities' 'trough of disillusionment." *Literature Compass* 14, no. 8 (August 1, 2017): no. pg.
- Jockers, Matthew Lee. “Chapter 8: Theme.” In *Macroanalysis: Digital Methods and Literary History*, 118–53. Topics in the Digital Humanities. Urbana: University of Illinois Press, 2013.

### Assignment
[Discussion post](https://utexas.instructure.com/courses/1216881/discussion_topics)

#### [▸ In-class outline](week-12.md)


----------------------------------------------------------------

## <a name="week14"></a>Week 14 (4/30): Final Presentations

[Final Presentation due](https://utexas.instructure.com/courses/1216881/assignments/4166564)

5/7: [Final Project due](https://utexas.instructure.com/courses/1216881/assignments/4166548)

----------------------------------------------------------------
# Additional resources:
**[Installation Tutorials](tutorials/)**
[Jeroen Janssens Seven Command Line Tools for Data Science (2013) workbench.](https://hub.docker.com/r/wlanderson/dsatclwb/)
Juola, P. and Ramsay, S. [Six Septembers: Mathematics for the Humanist](http://digitalcommons.unl.edu/zeabook/55/). Zea E-Books.
Karsdorp, Folgert. [Python Programming for the Humanities](http://www.karsdorp.io/python-course/)
Williamson, Evan Peter. [Fetching and Parsing Data from the Web with OpenRefine](https://programminghistorian.org/lessons/fetch-and-parse-data-with-openrefine#start-sonnets-project)
