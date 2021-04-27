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

<img src="https://www.pngfind.com/pngs/m/7-79122_under-construction-png-under-construction-clip-art-transparent.png" height="300" align="middle"  />

### Getting started
---------------------------------
The goal of this lesson is to introduce you to data reviews in GloBI.

At the end of this time we will regroup and report back the other workshop participants about what we did in this breakout group. Who would like to be the person/s who report back for the breakout group?

Let's collaboratively take notes in the Google Document. The link to the document is in the chat.

### What is a review
-----

A *review* in GloBI is an output that lets us know how GloBI interpreted or viewed the data being indexed. It is an opportunity to see if you agree with the interpretation or find issues in the data that can be corrected. It also provides some cool statistics about the number of interaction records indexed from a particular dataset. Reviews are done by dataset only. Reviews are useful for people who are submitting data, data curators, or anyone who wants to know more about a particular dataset.

### Finding the reviews
-----
[Data for all sources](https://www.globalbioticinteractions.org/sources)

[Data for Terrestrial Parasite Tracker](https://www.globalbioticinteractions.org/parasitetracker)


### What is what?
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


If you'd like, you can generate your own review notes by:
  - installing GloBI's Elton via https://github.com/globalbioticinteractions/elton
  - running "elton update globalbioticinteractions/ucsb-izc && elton review --type note,summary globalbioticinteractions/ucsb-izc > review.tsv"
  - inspecting review.tsv
~~~

### Exercise: Open a review file in Google Documents
-----
Take the review overview of one of the data reviews and import into a google spreadsheet. Here is an example of how this is done.

<img src="https://github.com/globalbioticinteractions/interaction-data-workshop/raw/gh-pages/fig/import-data.png" height="200" align="middle"  />



### Interpreting a review file
-----