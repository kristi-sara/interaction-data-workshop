---
title: "Data Sources: Interaction Data Record Review"
teaching: 15
exercises: 5
questions:
- "How can I understand how GloBI interpreted my dataset?"
- "Can GloBI help me improve my dataset?"
objectives:
- "Find out where GloBI reviews are located."
- "Find out how to explore GloBI reviews"
keypoints:
- "There are many ways to access GloBI reviews."
- "GloBI reviews can help data managers better understand their data and how GloBI interprets it."
---

### Goals
---------------------------------
> The goal of this lesson is to introduce you to data reviews in GloBI.

### Getting started
---------------------------------
> At the end of this time we will regroup and report back the other workshop participants about what we did in this breakout group. Who would like to be the person/s who report back for the breakout group?

> Let's collaboratively take notes in the Google Document. The link to the document is in the chat.

### What is a review
-----
> A *review* in GloBI is an output that lets us know how GloBI interpreted or viewed the data being indexed. It is an opportunity to see if you agree with the interpretation or find issues in the data that can be corrected. It also provides some cool statistics about the number of interaction records indexed from a particular dataset. Reviews are done by dataset only. Reviews are useful for people who are submitting data, data curators, or anyone who wants to know more about a particular dataset.

### Finding the reviews
-----
> Remember we explored in [working with data sources](https://www.globalbioticinteractions.org/interaction-data-workshop/05-working-with-data-sources/index.html) that all GloBI data sources are listed on the [sources](https://www.globalbioticinteractions.org/sources) page. In addition, [providers for Terrestrial Parasite Tracker](https://www.globalbioticinteractions.org/parasitetracker) have their own webpage.

> Let's examine a GloBI data review. Visit [https://globalbioticinteractions.org/sources](https://globalbioticinteractions.org/sources) and locate the **ucsb-izc** collection. Click on the <img src="https://depot.globalbioticinteractions.org/reviews/AgentschapPlantentuinMeise/ashForestInteractions/review.svg" style="display: inline; height: 1.1em; margin: 0;"> badge.


### What is what? An overview of the data.
-----
~~~
   _____ _       ____ _____   _____            _                
  / ____| |     |  _ \_   _| |  __ \          (_)               
 | |  __| | ___ | |_) || |   | |__) |_____   ___  _____      __ 
 | | |_ | |/ _ \|  _ < | |   |  _  // _ \ \ / / |/ _ \ \ /\ / / 
 | |__| | | (_) | |_) || |_  | | \ \  __/\ V /| |  __/\ V  V /  
  \_____|_|\___/|____/_____| |_|  \_\___| \_/ |_|\___| \_/\_/   
 | |           |  ____| | |                                     
 | |__  _   _  | |__  | | |_ ___  _ __                          
 | '_ \| | | | |  __| | | __/ _ \| '_ \                         
 | |_) | |_| | | |____| | || (_) | | | |                        
 |_.__/ \__, | |______|_|\__\___/|_| |_|                        
         __/ |                                                  
        |___/                                                   

Review of [globalbioticinteractions/ucsb-izc] started at [2021-04-26T06:04:32+02:00].

Review of [globalbioticinteractions/ucsb-izc] included:
  - 1440 interaction(s)
  - 25 note(s)
  - 1442 info(s)

[globalbioticinteractions/ucsb-izc] has 25 reviewer note(s):
      7 found unsupported interaction type with name: [Visiting]
      6 source taxon name missing: using institutionCode/collectionCode/collectionId/catalogNumber/occurrenceId as placeholder
      3 found unsupported interaction type with name: [Sitting on]
      3 found unsupported interaction type with name: [Hovering over]
      2 found unsupported interaction type with name: [Feeding on]
      1 found unsupported interaction type with name: [Visitng]
      1 found unsupported interaction type with name: [visiting]
      1 found unsupported interaction type with name: [Tended by]
      1 found unsupported interaction type with name: [Next to]
~~~

**1440 interaction(s)** is number of interactions indexed by GloBI from this dataset.

**25 note(s)** or rows in the dataset that are flagged and might be interesting to have a look at.

**1442 info(s)** or information about biotic interaction indexing process. These are not flagged records, but more like comments or data logging.

**6 source taxon name missing** where the taxon name field is blank or empty

**unsupported interaction type** indicates that no mapping is defined by the data source. Terms are defined by linking to the Relations Ontology.

### What is what? I want more information.
-----
>GloBI data reviews are packaged in downloadable text files (tab and comma delimited). The **review-sample** files are small enough to quickly view. 

~~~
This review generated the following resources:
  - review.svg (review badge) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review.svg
  - review.tsv.gz (data review) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review.tsv.gz
  - review-sample.tsv (data review sample tab-separated) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review-sample.tsv
  - review-sample.json (data review sample json) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review-sample.json
  - review-sample.csv (data review sample csv) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review-sample.csv
  - indexed-interactions.tsv.gz (indexed interactions) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-interactions.tsv.gz
  - indexed-interactions.csv.gz (indexed interactions) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-interactions.csv.gz
  - indexed-interactions-sample.tsv (indexed interactions sample) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-interactions-sample.tsv
  - indexed-interactions-sample.csv (indexed interactions sample) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-interactions-sample.csv
  - indexed-names.tsv.gz (indexed names) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-names.tsv.gz
  - indexed-names.csv.gz (indexed names) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-names.csv.gz
  - indexed-names-sample.tsv (indexed names sample) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-names-sample.tsv
  - indexed-names-sample.csv (indexed names sample) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-names-sample.csv
  - indexed-citations.tsv.gz (indexed citations) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-citations.tsv.gz
  - indexed-citations.csv.gz (indexed citations) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/indexed-citations.csv.gz
  - nanopub.ttl.gz (interactions nanopubs) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/nanopub.ttl.gz
  - nanopub-sample.ttl (interactions nanopub sample) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/nanopub-sample.ttl
  - review.zip (review archive) https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review.zip
~~~

### Get a glimpse of the review in Google Sheets
-----
>1 - Import a **review-sample** file into Google Sheets
><img src="../fig/import-data.png" height="200" align="middle"  />
>2 - Download the [full review archive](https://depot.globalbioticinteractions.org/reviews/globalbioticinteractions/ucsb-izc/review.zip)
>3 - Import the **indexed-interactions-sample.tsv** into Google Sheets


> ## `Exercise 1: Find Data Sources`
> Visit [https://globalbioticinteractions.org/sources](https://globalbioticinteractions.org/sources) and locate the **USNM Ixodes Collection**, Seltmann's > **Tick Interaction Database**, or **iNaturalist** observation records. For each, click on the <img src="https://depot.globalbioticinteractions.org/reviews/AgentschapPlantentuinMeise/ashForestInteractions/review.svg" style="display: inline; height: 1.1em; margin: 0;"> badge to open the review page. For one of the datasets:
1 - find out how many interactions have been indexed for each dataset.
2 - import the **indexed-interactions-sample.tsv** into Google Sheets
{: .challenge}
