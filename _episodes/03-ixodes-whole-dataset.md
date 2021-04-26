---
title: "Accessing the Whole Dataset"
teaching: 25
exercises: 5
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
- "Sharing code helps everyone!"

---

### Goals
-----

The entire "GloBI dataset" consists of over 6 million interaction records. There are many ways to approach a large dataset and this exercise is to demonstrate one example using Shell and R. We are not going to follow along with Shell and introduction to R tutorials in this workshop, but Carpentries has a few nice ones to get you started.
> [Introduction to Shell](https://swcarpentry.github.io/shell-novice/)

> [Introduction to R](https://datacarpentry.org/R-ecology-lesson/01-intro-to-r.html)


### Find all of the records in the dataset based on a taxon name
---------------------------------

We are interested in finding all of the records in the interactions.csv dataset that deal with Ixodes and we are interested in reducing the size of the data so it is easier to manage. One quick way to do this is via the Shell.

1 - How many records are in the GloBI dataset (interactions.csv-snapshot version). Its a lot!
> wc -l interactions.csv

2 - Extract and make a file of only the Ixodes records using Globi_Ixodes_Data.sh script. Explain that .sh will help reducde size of dataset than can use R. This will take ~ 4 minutes and 12 seconds!
> sh Globi_Ixodes_data.sh

3  - How many records are in the trimmed GloBI datasets? Is there a difference between unique and not?
> wc -l Ixodes_data.csv

> wc -l Ixodes_data_unique.csv

4 - Load trimmed dataset into R using R-studio
> [html preview](https://htmlpreview.github.io/?https://github.com/seltmann/globi-workshop-2021/blob/main/code/globi-example.html)


### Put dataset into sqlite database
---------------------------------

Databases are a great way to manage large datasets and handle data filtering, sorting and grouping. Sqlite is commonly used with R as it is easily transferable with the R code. We are not going to learn sqlite today, but there are some great Carpentries tutorials to get you started. 

> [Introduction to sqlite](https://swcarpentry.github.io/sql-novice-survey/)


Lets step through a few commands to see how easy it is to take a CSV file and create a sqlite database.

> sqlite3 globi.db

> .mode csv

> .import Ixodes_data_unique.csv interactions

> PRAGMA table_info(interactions);

> SELECT sourceTaxonGenusName, count(sourceTaxonGenusName) FROM interactions group by sourceTaxonGenusName;

> SELECT interactionTypeName, count(interactionTypeName) FROM interactions group by interactionTypeName;

> .exit

