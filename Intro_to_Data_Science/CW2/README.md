20MAP500: Coursework II

1 Overview

2 Instructions

3 Files to submit

4 Marking scheme

1 Overview

In this second assessed coursework, you will select some topic of interest about which you will form five research questions. You will operationalise these five questions and collect open data to answer them.


2 Instructions

Find a topic of interest along with five research questions that can be answered using data. Collect data that can be used to answer your five operationalised research questions. Note: As illustrated by the data-science life cycle discussed in class, the order of these steps may vary and may be highly non-linear. For instance, you may only be able to fully operationalise questions after seeing what data are available. Likewise, answering some questions may motivate new questions which in turn require additional data to be collected.

For the data collection you have multiple options:

collect data yourself (e.g. by manually filling in a spreadsheet or using a web scraper),
use existing open data sets (e.g. from online sources – see the slides for Lecture 3 for some suggestions) or
a mixture of a. and b.
Do not use any data set that has been already analysed as part of the lectures or computer labs.

If you collect data yourself, make sure that your data collection process follows clearly laid out rules that determine which data points are included in your data set. You should store your data in a .csv file. For instance, if you manually fill in a spreadsheet, use your favourite spreadsheet application to export your spreadsheet to .csv.

Your tidied data frame(s) should

comprise at least eight relevant variables each with at at least 200 observations (or at least 50 if you do not use existing data sets);
include at least one relevant variable that is a factor, character, date, or date-time;
include at least one relevant variable that is numeric, i.e. integer or double.
You can check the suitability of the dataset with me (i.e. the module leader) up until Thursday, 15 October 2020.

Provide answers to your five operationalised questions based on the data supported by meaningful visualisations.


3 Files to submit
You will submit your report (along with your data) in the form of a single R notebook (i.e..Rmd file) which contains your analysis and which can be rendered (“knitted”) to an .html document. Specifically, submit

any data set used for your analysis,
your R notebook (i.e. the .Rmd file),
the rendered .html version of your notebook (in case there are any problems knitting your .Rmd during marking).
Note: the total submission size must be less than 800 megabytes.

Edit (15 October 2020): do not include any identifying information such as your name anywhere in the submitted documents


4 Marking scheme

The report should be structured into the following sections.


Introduction [3 points]

Motivate your work, i.e.
briefly describe the topic,
briefly explain why it is worth studying.

Questions [20 points]

State five interesting research questions you study about the topic.
For each question, explain how you operationalise it.

Data [10 points]

Describe the data, i.e.
if you have collected data yourself, explain where and how the data were collected and which rules you have used to determine which data points to include in your data set,
if you use existing open data sets from some online source, state the source of the data so clearly that another person can retrieve the same data, the method by which they were originally collected and for what purpose,
summarise the variables contained in the data set(s) after any steps needed for cleaning and tidying the data,
if you need to exclude any observations from your analysis, justify this here.

Analysis [35 points]

Answer the five operationalised research questions.
Each answer should be supported by one or more meaningful visualisations.
Over the course of answering your five questions, you should
make use of at least eight variables in your data set,
have at least five meaningful visualisations which each rely on data from more than one variable.

Conclusion [2 points]

Summarise your results.
Mention at least one further question raised by the results of your analysis.
In addition, your project should satisfy the following conditions.

Reproducibility [10 points]

Ensure that your entire analysis is reproducible on another computer which has access to the raw data by knitting your R notebook. In particular, this means that
your project folder contains a folder data which holds all your data files, potentially organised into further subfolders as needed,
your notebook specifies the paths to the data using relative – not absolute – paths,
any data wrangling/data cleaning is done via the R code inside your notebook,
use of additional R packages is allowed.
Figure formatting [10 points]
Ensure that each of your graphs has suitably labeled and formatted axes and a suitable colour scheme, title and legend if appropriate.

Style [10 points]

Your knitted report should only show suitably formatted text and figures (and potentially tables). No code should be visible in the rendered document. It should be written in full text (i.e. not just bullet points) and in such a way that it can be read and understood by someone who has not seen the data, does not have access to the data, and has only general knowledge about the field of study.
Ensure that
you have checked your spelling and grammar, and you have ensured that all abbreviations are defined in the text,
your code layout and naming conventions for variables and functions follow a consistent style.
each column in your tidied data frame(s) has a suitable data type.
wherever necessary, you add meaningful comments to your code unless it is self-explanatory in the eyes of a person familiar with base R and any of the packages used in the lecture notes.
