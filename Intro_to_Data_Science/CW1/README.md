20MAP500: Coursework I
1 Overview
2 Instructions
3 Files to submit
4 Marking scheme
1 Overview
In this first assessed coursework, you will analyse data about bike rides undertaken by users of Capital Bikeshare (CaBi) – a publicly-owned bicycle sharing system that serves areas in and around Washington DC in the United States.

2 Instructions
Start a new RStudio project. Create a folder data within your project folder; within the data folder, create an empty folder named data_rides.

Go to https://www.capitalbikeshare.com/system-data and download the trip-history data for all rides started between the beginning of January 2019 and the end of July 2020. That is, the files you need to download are .zip files containing trip-history data stored in .csv files. Save these .zip files to /data/data_rides within your project folder. Do not extract the .zip files.

Under no circumstances should you modify the downloaded files in data_rides, neither manually nor through your code. Your R script should read the raw data directly from this folder.

Read the data from data_rides into a single tidy tibble called rides with (at least) the following columns:

duration: the length of the rides in seconds;
started_at: the starting date and time-of-day of the rides;
ended_at: the finishing date and time-of-day of the rides;
start_station_name: the name of the start station;
end_station_name: the name of the finishing station;
member_casual the membership type of the user (its values should be either “member” or “casual”). Hint: Search online for information about the pricing structure members or casual users.
Your R notebook should read the data from the files in data_rides without having to manually specify the name for each file (this ensures that your code still works if we add new files into data_rides. Hint: attempting to directly bind the rows of the data sets in these files together may throw an error because the data type of one of the columns is not consistent across in different files. You may find the functions is.factor() and as.factor() helpful). Edit (15 October 2020): there is a typo in this hint. Please see the additional file cw1_erratum_and_further_hint.html for a correction and for an updated hint.

Don’t forget to ensure that each column in rides has an appropriate data type, e.g. factor, integer, character, Duration, datetime etc.

Find five interesting questions raised by the data in rides. For instance, you could investigate how the COVID pandemic has changed rental bike usage patterns.

Provide answers to your five operationalised questions based on the data supported by meaningful visualisations.

3 Files to submit
You will submit your report in the form of a single R notebook (i.e..Rmd file) which contains your analysis and which can be rendered (“knitted”) to an .html document. Specifically, submit

your R notebook (i.e. the .Rmd file),
the rendered .html version of your notebook (in case there are any problems knitting your .Rmd during marking).
Note: the total submission size must be less than 800 megabytes.

Edit (15 October 2020): do not include any identifying information such as your name anywhere in the submitted documents.

4 Marking scheme
The rendered report should be structured into the following sections.

Introduction [3 points]
Motivate your work, i.e.
briefly describe the topic,
briefly explain why it is worth studying.
Data [10 points]
Describe the data set, i.e.
briefly explain the source of the raw data,
summarise the variables contained in the data set after any steps needed for cleaning and tidying the data,
if you need to exclude any observations from your analysis, justify this here.
Questions [20 points]
State five interesting research questions raised by the data,
For each question, explain how you operationalise it.
Analysis [35 points]
Answer the five operationalised research questions.
Each answer should be supported by one or more meaningful visualisations.
Over the course of answering your five questions, you should
make use of each of the following variables contained in rides: duration, started_at, ended_at, start_station_name, end_station_name and member_casual,
have at least five meaningful visualisations which each rely on data from more than one variable,
use each of the following elements in one or more of the graphs:
faceting;
meaningful annotation;
discrete colour or fill scales (i.e. discrete variable mapped to the colour or fill aesthetic);
continuous colour or fill scales (i.e. a continuous variable mapped to the colour or fill aesthetic).
Conclusion [2 points]
Summarise your results.
Mention at least one further question raised by the results of your analysis.
In addition, your project should satisfy the following conditions.

Reproducibility [10 points]
Ensure that your entire analysis is reproducible on another computer which has access to the raw data by knitting your R notebook. In particular, this means that
your project folder contains a folder data which holds all your data files organised into further subfolders as specified in the instructions above,
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
each column in your data frame (e.g. in rides) has a suitable data type.
wherever necessary, you add meaningful comments to your code unless it is self-explanatory in the eyes of a person familiar with base R and any of the packages used in the lecture notes.
