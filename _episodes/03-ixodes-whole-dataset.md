---
title: "Analysis of Ixodes (ticks) Records using Whole Dataset"
teaching: 15
exercises: 5
questions:
- "Question 1"
- "Question 2"
objectives:
- "Objective 1"
- "Objective 2"
keypoints:
- "key point 1"
- "key point 2"
---



goes over demo / worksheet of the ixodes whole dataset

1 - Navigate to the https://www.globalbioticinteractions.org/data page. What ways exist to get the data and what are the differences?
![GloBI Data Page](/photos/data.png)

2 - How many records are in the GloBI dataset (interactions.csv-snapshot version). Its a lot!
> wc -l interactions.csv

3 - Extract and make a file of only the Ixodes records using Globi_Ixodes_Data.sh script. Explain that .sh will help reducde size of dataset than can use R. This will take ~ 4 minutes and 12 seconds!
> sh Globi_Ixodes_data.sh

4  - How many records are in the trimmed GloBI datasets? Is there a difference between unique and not?
> wc -l Ixodes_data.csv

> wc -l Ixodes_data_unique.csv

5 - Load trimmed dataset into R using R-studio
> [html preview](https://htmlpreview.github.io/?https://github.com/seltmann/globi-workshop-2021/blob/main/code/globi-example.html)

6 - Put entire dataset into SQLlite database
![GloBI Data Page](/photos/sql.png)
> sqlite3 globi.db

> .mode csv

> .import Ixodes_data_unique.csv interactions

> PRAGMA table_info(interactions);

> SELECT sourceTaxonGenusName, count(sourceTaxonGenusName) FROM interactions group by sourceTaxonGenusName;

> SELECT interactionTypeName, count(interactionTypeName) FROM interactions group by interactionTypeName;

> .exit

