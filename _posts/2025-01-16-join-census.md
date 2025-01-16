---
layout: post
title: "Census Data"
---

## Accessing Census Data

- Census API 
- tidycensus package
- the geographic scale of social media data is best suited for analysis at the county or even state level.

## Mapping Census Data

- choosing variables
- normalizing by population
- classification types
- choropleth maps with ggplot

## Spatial Joins

Spatial joins are accomplished much like an attribute join, but the `by` criteria for matching data is replaced with a spatial relationship.

After joining, we need to `count` how many tweets occurred in each county.

## Mapping Twitter Data

- Normalizing tweets by meaningful denominators (e.g. people, households, population aged 15-65)

## Assignment Markdown File

- The notes and guide for today are again in the form of an [Rmarkdown file](https://drive.google.com/open?id=1FDQR5dQo5A3TA3KKed6K_ao1GWyVtfTh&usp=drive_fs). 
- Save this into your `scripts` folder, open your RStudio project and proceed from there! 
- This notebook is independent of previous assignments, so it's fine to clear the R environment as you begin.
- Wherever you find an ellipsis `...` in the code, you'll need to complete the code on your own.