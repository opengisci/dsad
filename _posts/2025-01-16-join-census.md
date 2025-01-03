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
- normalizing
- classification types
- choropleth maps with tmap

## Spatial Joins

Spatial joins are accomplished much like an attribute join, but the `by` criteria for matching data is replaced with a spatial relationship.

After joining, we need to `count` how many tweets occurred in each county.

## Mapping Twitter Data

- Normalizing tweets by meaningful denominators (e.g. people, households, population aged 15-65)