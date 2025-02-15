---
layout: post
title: "Disaster Data"
---

## Guest Speaker

- Surprise! Alumnus Liam Smith will join us at the beginning of class to speak about his experience learning data science and applying it to an internship with the National Park Service. [Some Links](https://docs.google.com/document/d/1ye3qI0mlQXvzvh31zMydYT6Qh3KtTUpzQvMN5X1vyxQ/edit?tab=t.0)

## A Forum

- We have a private repostiory for the class on which you can post discussion questions and answers: [https://github.com/opengisci/dsad_forum/discussions](https://github.com/opengisci/dsad_forum/discussions)

## Twitter/X Social Media Data

- Characteristics of ``big data'' generally and Twitter/X specifically
- Legal and ethical constraints and considerations
- Twitter application programming interface and queries
- Twitter metadata and example Tweet
- [slides](https://drive.google.com/open?id=122vhIvRJ7Xys8Oyvppb5V_3gBn879b0a&usp=drive_fs)

## Data Science Tools and Organization

- Structure your project with folders for:
  - `data_raw` (for unmodified given files) `data_private` (for very large or secret files), and `data_derived` (for data files you create to share)
  - `docs` for your final documents or websites, e.g. your rendered `.html` files. GitHub and GitLabs use the `docs` folders to make websites like this one from repositories
  - `code` or `scripts` for, you know... your code.
- Project management files
  - `.Rproj` is at the root of an R project and maintains information about the `.RData` file, any version control, and what files you have had open
  - `.RData` contains *all* data loaded in the R Environment (i.e. everything in the environment pane). It is convenient for temporary use on a local computer (e.g. for shutting down your computer after lecture and re-opening your project after lunch), but it is major problem to rely on it in the context of reproducibility, Git, and collaboration across different computers and team members.
  - `.gitignore` contains items & instructions for which files Git and GitHub should ignore.
  - `.Rproj.user` folder contains temporary files for the R project. Pay no attention.
  - `.git` folder contains essential information about the Git repository, e.g. the history of commits. Git maintains this folder and it is important for Git version control, so you should leave it alone. It may even be hidden from you.
- `here` package helps you manage links to files
  - starts looking for files in the root folder of the project (where Rproj file is, or where Git repository starts)
  - searches for files and folders in a sequential list and builds an operating-system specific file path: e.g. `here("data", "givens", "mytable.csv")` will find `"\data\givens\mytable.csv"`

Managing the folder structure with Git:

 - Add `data_private\` to your `.gitignore` so that private things will not be tracked
 - commit the changes to `.gitignore`
 - Git pays no attention to folders until they have content inside


### Create a new folder with codde

The following line of code can check if a folder exists and if not, create it.

```r
if(!dir.exists(here("data_private"))) {dir.create(here("data_private"))}
```

We can break down how it works below:

Code | Purpose |
| :--: | :--: |
`here(“data_private”)` | creates a path to a `data_private` folder in your project |
`dir.exists(here(“data_private”)` |   	checks if the folder is there, resulting if `TRUE` if it is, and `FALSE` if it is not. |
`!dir.exists(here(“data_private”)`  | 	`!` negates the above, equivalent to checking if a folder does NOT exist
`if( …  )  { …  }`	|	`if()` controls flow of code. If whatever is in the `( parenthesis )` is `TRUE`, then do the stuff inside the `{ curly brackets }`. Otherwise, skip the stuff in curly brackets. |
`dir.create(here("data_private"))`	| makes a new folder

### Example demo repository

 [Example Repository Structure and File Management](https://github.com/opengisci/wt25_demo)

# First Assignment

Let's start analyzing this data by investigating some preliminary questions about it's quality and structure.

- How many tweets are there?
- How many tweets are tagged with geographic coordinates?
- How many tweets are tagged with a place name, and how many are there by each place type?
- Which users have the most followers, retweets, or quotes?
- How many tweets are there from each country in the dataset?
- Graph the frequency of tweets over time, by different time increments

Submit the first assignment by completing an Rmarkdown document and knitting it, including a graph of how many tweets are tagged with place names of which types, and another interesting and creative graph from this dataset.

Data is available in this private repository [github.com/opengisci/Data-Restricted](https://github.com/opengisci/Data-Restricted)

## Transactions

- Computational Notebooks are due Friday at 12 noon
- First Assignment is due Monday at 5pm
- There is one article to read for the Tuesday Workshop
