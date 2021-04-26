---
title: "Getting Interaction Data"
teaching: 15
exercises: 10
questions:
- "Where can I download interaction data?"
- "What formats are the data available?"
objectives:
- "Understand the available ways to get interaction data"
- "Understand the columns of the downloaded data"
keypoints:
- "GloBI has interaction data that can be accessed as a full dataset"
- "Better to use the full dataset than the APIs"
---


### Goals
-----

<img src="https://www.globalbioticinteractions.org/assets/globi.svg" height="100px" align="left"  />
Let's get oriented with the interaction data found on GloBI.

### Where to find data
-----

Navigate to the https://www.globalbioticinteractions.org/data page.


### What is what?
-----

<img src="https://github.com/globalbioticinteractions/interaction-data-workshop/raw/gh-pages/fig/interaction-data.png" height="400" align="middle"  />

*stable* versions of the data are versioned in the [doi:10.5281/zenodo.3950589](https://zenodo.org/record/3950590)GloBI data publication.
*snapshot* are the most recent versions. Thus, this could change daily! Great for exploration and preliminary analysis.

### Data publication
----
For research or other data intensive project, it is suggested to use GloBI’s stable versioned integrated data published via [doi:10.5281/zenodo.3950589](https://zenodo.org/record/3950590) or create a new data publication that contains the data you are using.


### Other ways of accessing GloBI data
-----

Exploratory, interactive queries can be executed through SPARQL and Cypher endpoints, GloBI Search/Browse pages, or by using the REST-y GloBI Web API. For those that use R, rglobi is available to explore interaction data. rglobi can also be used to execute Cypher queries. However, it is best to consider these as methods for exploring data rather than data access points. **If you are doing research, download the full dataset and create a version of it**.

