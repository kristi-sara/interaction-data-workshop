---
title: "Working with the Whole Dataset"
teaching: 20
exercises: 10
questions:
- "How can I get started with the whole interaction dataset?"
- "Is this the only way to manage the interaction dataset?"
objectives:
- "Trim the dataset to only records that contain *Ixodes*"
- "Put dataset into R and poke around"
- "Add dataset to sqlite database"
- "Learn from each other and ask questions!"
keypoints:
- "There is a lot of interaction data available and shell is one helpful tool to reduce the size of the dataset."
- "Sharing code helps everyone."

---

### Goals
-----
> The entire or whole interaction dataset on GloBI consists of over 6 million interaction records. There are many ways to approach a large dataset and this exercise is to demonstrate one example using shell and R. We are not going to follow along with shell and introduction to R tutorials in this workshop, but Carpentries has a few nice ones to get you started, including [Introduction to shell](https://swcarpentry.github.io/shell-novice/) and [Introduction to R](https://datacarpentry.org/R-ecology-lesson/01-intro-to-r.html).

> These exercises can be followed along using R and shell, but it is not necessary. If you would like to follow along, please go ahead and open R-studio and your shell window.

### Getting started
---------------------------------
> At the end of this time we will regroup and report back the other workshop participants about what we did in this breakout group. Who would like to be the person/s who report back for the breakout group?

> Let's collaboratively take notes in the Google Document. The link to the document is in the chat.

### Find all of the records in the dataset based on a taxon name
---------------------------------
> We are interested in finding all of the records in the interactions.csv dataset that deal with *Ixodes* and we are interested in reducing the size of the data so it is easier to manage. One quick way to do this is via the shell.

> How many records are in the GloBI dataset. It is a lot!

~~~
wc -l interactions.csv
~~~

> One of the first things we might want to do is trim the dataset to only those taxa we are interested in analysing. In this case, we will look for all *Ixodes* records. To do so, we will use a simple [shell script](https://github.com/seltmann/interaction-data-workshop), extract all of the rows that contain the word *Ixodes* and create a new file file. This process will help reduce the size of the dataset so we can use R for our analysis. The shell script will take ~ 4 minutes and 12 seconds to complete!

~~~
sh Globi_Ixodes_data.sh
~~~

> When we examine the code in the script we see that it is using grep, which is "a Unix command used to search files for the occurrence of a string of characters that matches a specified pattern". Grep matches on the row and does not specify which column *Ixodes* is found. We then sort the records to look for only exact, unique versions of the records.

~~~
echo Creating headers
head -1 ../data/interactions.csv > ../data/Ixodes_data.csv

echo Finding all Ixodes
cat ../data/interactions.csv | grep -w "Ixodes" >> ../data/Ixodes_data.csv
wc -l ../data/Ixodes_data.csv

echo Sorting unique records
sort -r ../data/Ixodes_data.csv | uniq > ../data/Ixodes_data_unique.csv
wc -l ../data/Ixodes_data_unique.csv
~~~

> If you want to find several taxa and combine the datasets, you could create files from multiple taxa and combine the output together into a single dataset using **cat**. An example of this can be found [here](https://github.com/lee-michellej/globi_tritrophic_networks/blob/master/Code/Globi_bee_data.sh). This example takes all files of the files in the Data folder that contanin the pattern **unique.tsv** and creates a new file called *all_data.txt**._

~~~
cat ../Data/*unique.tsv >> ../Data/all_data.txt
~~~

> Now lets compare the new datasets.How many records are in the trimmed GloBI datasets? Is there a difference between unique and not?

~~~
wc -l Ixodes_data.csv

wc -l Ixodes_data_unique.csv
~~~

### Let's do something in R
---------------------------------
> Load trimmed dataset into R using R-studio. We will start by stepping through some R code and discuss the results. The [R code](https://github.com/seltmann/interaction-data-workshop) we are using can be downloaded to follow along or you can see an [html preview](https://htmlpreview.github.io/?https://github.com/seltmann/globi-workshop-2021/blob/main/code/globi-example.html) of the code.

> We will start by just finding the columns and create a subset of the data to import into Google Sheets. Time permitting, we will talk about some of the interesting data issues we are finding in the dataset. 

> ## `Exercise 1: What do the columns mean?`
-----
> There are 88 columns in the interactions data file. In this exercise, we will find the columns and pick out which ones are commonly useful in research data. You can create your own list or use this Google Sheet with the first [100 rows of the Ixodes_data_unique.csv](https://docs.google.com/spreadsheets/d/10C4VnpPZnq5LbaMorVcU8EWTXlI7-dbpg7az-_GKIVI/edit?usp=sharing) file.
1. Obtain a list of all of the column names.
2. How many of them deal with taxon names?
3. What column/s include the citation information?
4. What column/s contains the interaction information?
5. What is the difference between the *source* and *target* columns?
5. Describe one other important column.
{: .challenge}


> ## `Import into a sqlite database`
---------------------------------
>Databases are a great way to manage large datasets and handle data filtering, sorting and grouping. Sqlite is commonly used with R as it is easily transferable with the R code. We are not going to learn sqlite today, but there are some great Carpentries tutorials to get you started, including the [Introduction to sqlite](https://swcarpentry.github.io/sql-novice-survey/). Let's step through a few commands to see how easy it is to take a CSV file and create a sqlite database.
{: .callout}

~~~
sqlite3 globi.db

.mode csv

.import Ixodes_data_unique.csv interactions

PRAGMA table_info(interactions);

SELECT sourceTaxonGenusName, count(sourceTaxonGenusName) FROM interactions group by sourceTaxonGenusName;

SELECT interactionTypeName, count(interactionTypeName) FROM interactions group by interactionTypeName;

.exit
~~~
