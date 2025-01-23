---
layout: post
title: "Final Projects"
---

## Reading for Discussion

- Kasperson, R. Renn, O., Slovic, P, Brown, H., Emel, J., Goble, R., Kasperson, J., Ratick, S. (1988). The social amplification of risk: A conceptual framework. *Society for Risk Analysis*, 8(2), 177–187. https://doi.org/10.1111/j.1539-6924.1988.tb01168.x [download](https://drive.google.com/open?id=121KAXNN4gYgc1r1qpr_-DRYGfwej_xO-&usp=drive_fs)

The reading above is often cited in hazard, risk and disaster literature as a framework for thinking about communication systems and the perils of incomplete or inaccurate information. 
Although it was written prior to the invention and widespread adoption of social media, the implications are clear.
How could this framework help inform your final project research questions and analyses? 

## Hurricane Ida

- [wikipedia](https://en.wikipedia.org/wiki/Hurricane_Ida)
- [Gulf Coast updates](https://www.nytimes.com/interactive/2021/us/hurricane-ida-tracker.html)
- [Northeast updates](https://www.nytimes.com/live/2021/09/03/nyregion/nyc-flooding-ida#de-blasio-storm-alerts)
- [devestation in Northeast](https://www.nytimes.com/2021/09/02/nyregion/ida-flooding-nyc.html)
- [power plant in New Orleans](https://www.nytimes.com/2021/09/10/us/ida-new-orleans-power.html)

## Third assignment

Complete the Hurricane Dorian spatial cluster analysis and Knit to an `html` file.  
To this analysis, add some experimentation with the Getis Oord method by trying at least two additional iterations of the analysis in which you adjust at least two of:
- alter the calculation of tweet rate by changing the multiplication factor, e.g. map tweets per 100 people or tweets per 100,000 people
- make `0`'s (counties with no twitter activity) to be `NA`
- select fewer states to map

Write some interpretation after the additional maps: how do the results change?
Why do you think that they change in this way?
One paragraph per map is good.

## Graphing Social Networks

We can construct graph models of social networks by measuring associations between users. 
These can be defined by the frequency and direction of interactions on the social media platform. 
Common interaction types include following, liking, reposting/retweeting, and replying. 
Social media users become *nodes* (points) in the network, and their interactions become *edges* (connecting lines). 
From there, all sorts of network characteristics can be visualized and calculated! 

## Bookdown

If all of the Rmd files in your repository can individually knit to an `html` file, you can use `Bookdown` to knit them into a digital book! 
See [bookdown.org/](https://bookdown.org/)

Some advice:  

- Install and load the `bookdown` package 
- Restart R 
- Create a new bookdown project and check out the file structure it creates
- Rmd files are added to the book in alphabetical order by default
- Code chunks must all have unique names or be unnamed (e.g. `setup` is a problem)
- Chapters start with first-level headings, e.g. `# Introduction`
- Building to `html` webiste format is the most straightforward. Building to `pdf` requires `LaTeX` software to be installed.
- Once everything is in place, you'll have a `build` panel with build options and ability to start the build.
- All the code is run, so it takes quite some time. Start small with just a few .Rmd files

## Final Project Tidbits

- Store all shiny app content in one folder, including data required of the app
- Only use cleaned and anonymized data in the app
- Prepare the data separately, using code in Rmd files
- There are supposedly `tmapOutput()` and `renderTmap()` functions
- You can add multiple tabs / pages to an app
- If you want something like a time animation, use sliders
- We could lean up twitter text better, either with regex expressions (as we saw in class with stringr package) or maybe a deprecated tidytext function `unnest_tweets()`, if it still works.
- We know how to geocode now, but it is a large amount of data!
  - First select for *unique* place data so that each place is only geocoded once.
  - Maybe geocode in batches, or test just a few places first
  - Save results immediately 
  - *Then* join x and y data back to the full set of tweets. 
  - Set the code block to eval=FALSE
  - Do NOT geocode an address more than once.
- GitHub is made for teamwork. It works best if you:
  - Always `PULL` before starting work or committing anything
  - Work on *different* files in parallel. Simultaneous work can be integrated seamlessly if the work was done in different files. E.g. you may have a couple of different Rmd files at first, and then integrate them later.
  - Only have one person make changes to the Shiny app at a time.
  - Use issues or discussion to track progress and communicate when not in person (i.e. don't duplicate information on email or other platforms: keep communications in one place-- attached to the work itself)

[igraph](https://r.igraph.org) is a popular package for building, analyzing, and visualizing graphs in R. 
The late [rtweet](https://github.com/ropensci-archive/rtweet) package had a convenient function for building an igraph from twitter data on retweets, mentions, quotes, and replies.
This package has been archived, and I've decided *not* to sort out a work around for it this semester.

## Final Project Groups

Groups of two to four students will be formed based on prior experience and research interest.

## Final Project Expectations

- Investigation of Hurricane Ida
- An insightful **Geographic Research Question** that can be answered with analysis and visualization of social media and Census data.
- **Data Analysis** using R code that is reproducible, legible, and well-documented with Rmarkdown.
- **Data Visualization** of your results with a Shiny app integrating multiple visualization types and some narrative with an emphasis on *legibility* and *telling an insightful story*. Project should somehow investigate relationships between time, geographic space, the storm (track and strength), society (as shown in characteristics of Twitter users and/or content), and demographic or socio-economic characteristics (from Census).
- **Interpretation** to tell a story with the data, addressing your research question. This may not actually be written in the app itself, but you should draft a storyline / path through the data visualization for your presentations and save it in the readme or your markdown file.
- **Attribution** of sources for all data, software, ideas, and any authorized use of code (e.g. from a tutorial or worked example online). 
- **Presentation** of the final project to the full DSAD class (Thursday 10:25 to 10:55)
- **Submission** of the final code repository on GitHub by noon EST of Friday, January 31.

- Data for final projects is available in a private repository: [github.com/opengisci/opengisci_restricted](https://github.com/opengisci/opengisci_restricted)

## Cheat sheets

- [sf]({{site.baseurl}}/assets/sf.pdf)
- [shiny]({{site.baseurl}}/assets/shiny.pdf)
- [tidytext]({{site.baseurl}}/assets/tidytext.pdf)
- [stringr]({{site.baseurl}}/assets/strings.pdf)
