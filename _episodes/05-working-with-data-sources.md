---
title: "Working with Data Sources"
teaching: 5
exercises: 2
questions:
- "How does GloBI discover interaction data?"
- "How does GloBI integrate interaction data?"
- "Is GloBI a data repository or a search index?"
objectives:
- "Understand where to find GloBI data sources"
- "Understand where to find GloBI data reviews"
keypoints:
- "GloBI is built using existing data sources"
- "Data sources are continously and automatically indexed by GloBI"
- "GloBI provides automated reviews of data sources"
---

Global Biotic Interactions (https://globalbioticinteractions, GloBI) relies on existing species interaction datasets, or data sources. These data sources are regularly automatically re-indexed by GloBI to include recent updates. So, rather than a data management system or repository, GloBI is more like a search engine that helps find biotic interaction data in openly available datasets.

The kinds of data sources indexed by GloBI are pretty diverse: some datasets come from professionally managed natural history collections or specialized data portals, whereas others are manually transcribe interaction records from literature, or observation records provided by citizen scientists. 

A list of GloBI data sources can be found at https://globalbioticinteractions.org/sources .

Exercise 1. Visit https://globalbioticinteractions.org/sources and locate the USNM Ixodes Collection, Seltmann's Tick Interaction Database, and iNaturalist observation records. For each, click on the GloBI badge to inspect some of the indexed interactions.

To build GloBI's interaction data search index, the following steps are taken:

1. **F**ind registered interaction data in Github and Zenodo. 
2. **A**ccess/download and version digital dataset 
3. **I**ntegrate interaction records using translation tables into a knowledge graph
4. allow for **R**euse by publishing integrated data products and services

These steps are repeated regularly, often many times a week, to include new additions or other updates.

Exercise 2. Visit https://globalbioticinteractions.org/process and describe the GloBI indexing process in your own words. 

To help better understand how GloBI interprets data sources, automated data reviews are made available for each data source. These dataset specific reviews include lists of review notes and summaries (e.g., review.tsv files), checklists of taxonomic names (e.g., indexed-names.tsv) and indexed interaction data records (e.g., indexed-interactions.tsv). 

Exercise 3. Visit the GloBI's Parasite Tracker project page at https://globalbioticinteractions.org/parasitetracker#CAS and locate the California Academy of Sciences / Entomology Collection. Click on each of the buttons and describe the function of the "review", "GloBI", "config", "issues" and "names" badges.

<a href="https://globalbioticinteractions.org/parasitetracker"><img src="../fig/globi-review.png"/></a>

