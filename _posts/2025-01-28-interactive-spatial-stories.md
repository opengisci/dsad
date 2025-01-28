---
layout: post
title: "Interactive Spatial Stories"
---

## Loops to close

- Assignment 3: variants of Getis-Ord cluster analysis
- Managing data for group projects
  - challenges with Git?
  - Census & other government data can go in the public folder 
  - Save documentation about metadata (e.g. dictionary of column names)
  - Prep the simplest, most anonymized RDS data files possible for the app
  - if you must map points, consider randomizing the location somewhat
- How Prof Holler [geocoded profile data](https://drive.google.com/drive/folders/1a308sFHQ_LyN9hvuIrSpKCw-nGuf5_Ny?usp=sharing)
- Is the geography of New York City a problem?
- Presentations: 6 minute story with Question, app driver & narrator(s). Focus on your findings and to some extent your achievements, not your struggles
- `qdapRegex` package has some useful text cleaning functions for Twitter text, including `rm_twitter_url`,  `rm_url`, `rm_tag`, and `rm_hash`. It also has some functions for address components.

## Possible Project Improvements

- You may use a batch of [geocoded profile locations]({{site.baseurl}}/assets/profile_geocodes.RDS)! Just join this table to the Tweets by the location column and integrate these coordinates into your analysis as the 3rd best option for mapping a Tweet.
- You may download other datasets from the Census or American Community Survey to include more detailed socio-economic information. Here is a [video tutorial](https://midd.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx?folderID=de8af8be-98b6-4758-bbc1-b126015b09e4) from GEOG 261. You don't need any of the QGIS stuff... the first few videos are a tour of Census data and techniques to download it using `tidycensus`.
- You may download data on storm impacts from NOAA's database. Bulk downloads are available by year, and choose the "details" data series (as opposed to just "locations") [NOAA storm events](https://www.ncdc.noaa.gov/stormevents/ftp.jsp)
- You may download data on the counties included in Federal Disaster Declarations from [FEMA](https://www.fema.gov/openfema-data-page/disaster-declarations-summaries-v2). Hints: filter the CSV file by `year`, by `incidentType`, and having "Ida" in the `declarationTitle`. To join to counties, notice that the placeCode is a 5-digit code composed of the state (2 digits) and county (3 digits), which should be equivalent to county `GEOID`'s. This data does not indicate how much damage, other than whether there was enough to cross the threshold to provide individual assistance (`iaProgramDeclared`). 
- Clean tweet text with general expressions

## Examples of Great Stories

- Hurricane Harvey [mapping destruction](https://www.nytimes.com/interactive/2017/08/24/us/hurricane-harvey-texas.html) and [cries for help](https://www.nytimes.com/interactive/2017/08/30/us/houston-flood-rescue-cries-for-help.html) and [lost in the storm](https://www.nytimes.com/interactive/2018/08/30/magazine/hurricane-harvey-houston-floods-texas-emergency.html)
- [Poison in the Air](https://www.propublica.org/article/toxmap-poison-in-the-air)
- [How much hotter is your hometown?](https://www.nytimes.com/interactive/2018/08/30/climate/how-much-hotter-is-your-hometown.html)


## Best Practices

- Be clear about the "universe" of your data. What population does the data represent? Is it a complete enumeration or a sample?
- Use consistent symbology, colors, fonts, and classification schemes
- Keep interactive graph axes constant
- Cite and link data sources and any significant sources of code

Thanks to Librarian Julia Deen for these resources:

- https://medium.com/agoda-engineering/10-common-data-visualization-mistakes-and-how-to-avoid-them-e3896fe8e104
- Wong, B. Gestalt principles (Part 1). Nat Methods 7, 863 (2010). https://doi.org/10.1038/nmeth1110-863
- Wong, B. Gestalt principles (Part 2). Nat Methods 7, 941 (2010). https://doi.org/10.1038/nmeth1210-941 
- Wong, B. Points of view: Points of review (part 2). Nat Methods 8, 189 (2011). https://doi.org/10.1038/nmeth0311-189Wong, B. Color coding. Nat Methods 7, 573 (2010). https://doi.org/10.1038/nmeth0810-573
- Krzywinski, M., Wong, B. Plotting symbols. Nat Methods 10, 451 (2013). https://doi.org/10.1038/nmeth.2490
- Gehlenborg, N., Wong, B. Mapping quantitative data to color. Nat Methods 9, 769 (2012). https://doi.org/10.1038/nmeth.2134
- Gehlenborg, N., Wong, B. Heat maps. Nat Methods 9, 213 (2012). https://doi.org/10.1038/nmeth.1902


## Citation


- Software: list the R version and the packages used for your work
- Data: Who created it? Where is it available (link, or ? When did you acquire it? 
- Literature: Authors, year, and DOI link (e.g. https://doi.org/...)

List this citational information both *in the app* and on the project's `README.md` file.