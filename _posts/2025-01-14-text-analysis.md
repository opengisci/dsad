---
layout: post
title: "Text Analysis"
---

## Reading for discussion

What can you do with spatial data science? Things [like this](https://www.nytimes.com/interactive/2025/01/09/us/la-wildfires-damage-photos-map.html?smid=url-share)

- Zou, L., Lam, N. S. N., Cai, H., & Qiang, Y. (2018). Mining Twitter Data for Improved Understanding of Disaster Resilience. Annals of the American Association of Geographers, 108(5), 1422–1441. https://doi.org/10.1080/24694452.2017.1421897 [download](https://drive.google.com/open?id=12-Z5TxKeNYCCB_eEHpO653aJUz41wiw4&usp=drive_fs)

Questions for discussion: 

-	What research questions are the authors asking?
-	How do the authors deal with the problem of unequal Twitter participation over space? (both due to uneven population over space and due to uneven social media use by people) 
-	How do the authors analyze the timing of twitter activity?
-	How does sentiment analysis work and what do the outputs of sentiment analysis mean? 
-   What is the story/interpretation of the tables and figures in the paper? 

## Time and Text Analysis

Wrapping up lecture...

- First, `pull` any changes into your local computer or, if you are using a new computer, `clone` your repository from scratch.
- I suggest adding a `data_public` folder to your repository, and save the `Life_Expectancy.csv` file into it.
- When you attend the next lecture, use the path `here("data_public", "Life_Expectancy.csv")` to load your data from CSV file. 

Organizing today...

- Please save [this Rmd file](https://drive.google.com/open?id=1FAykkoG7KE0I6Dpoti0HbwgAbOgPXVFD&usp=drive_fs) into your scripts folder.
- We'll follow along with this instructional `Rmd` file today!

## Date-time data

- We've been treating years as integers so far, but it's not so easy when time includes the month, day, hours and minutes.
- Dates require special `date` data types. For Twitter, it's `POSIXct`
- You should expect to treat dates differently, and use special functions like `as.POSIXct` to create them
- `ggplot` even has a special axis function `scale_*_datetime` type for temporal data

## Cleaning Text

- non-text
- stop words
- search terms
- `unnest` text content into `tokens`
- can we remove handles, e.g. `@nytimes` from text content?

## Word Frequency

- histograms
- word graphs

## Word Association

- `n-grams` are pairs of words found in sequence 
- we can count common co-occurences of words
- build a graph data model of them
- and visualize the graph!