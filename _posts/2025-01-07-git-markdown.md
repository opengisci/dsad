---
layout: post
title: "GitHub and RMarkdown"
---

## Reading for Discussion

Please read the following article prior to our Tuesday afternoon meeting.  
The article demonstrates the types of data and analysis that we will learn to accomplish during this winter term. In our first pass through the article, our goal is to get a sense of the types of graphs, maps, and information the authors have extracted from social media data.

Wang, Z., Ye, X., & Tsou, M. H. (2016). Spatial, temporal, and content analysis of Twitter for wildfire hazards. *Natural Hazards*, 83(1), 523–540. https://doi.org/10.1007/s11069-016-2329-6 (download)[https://drive.google.com/open?id=12-Etp7vqxi245qov-hU8-496U8z-xuav&usp=drive_fs]

## Git and GitHub

- Git software [git-scm.com/](https://git-scm.com/)
- GitHub account [github.com/](https://github.com/)
- What is version control?
- Advantages of using Git version control for Data Science

### Key Git and GitHub Actions

- `Clone`: Download a repository (yours or someone else's) to a local computer
- `Fork`: Make a copy of a repository (yours or someone else's) in your own online GitHub account. This copy may maintain association with the original repository.
- `Commit`: Save a batch of changes to your repository, including a brief message and description
- `Revert`: Undo one or more commits.
- `Push`: Upload one or more commits from the local computer to the GitHub servers
- `Pull`: Download commits from the GitHub servers to your local computer and merge them into your repository. Or, if you have forked a repository and the original repository has continued to commit revisions, `pull` the revisions from the original version into your own forked version. An example case of this: you fork a repository with a course assignment and the professor subsequently makes a last-minute revision to the assignment. Just pull the changes into your own version!
- `Pull Request`: Send suggested commits from your own forked version of a repository to the original repository owner. An example case of this: you fork a version of an open source GIS plugin, fix some errors or make some improvements, and send suggested revisions back to the plugin developer.

## Personal Course Repository

Professor Holler will create a private personal respository in which each student can store course notes and recieve individual feedback. In a workshop activity, we will practice using GitHub, Git, and RStudio to transfer information between laptops and lab computers, and [GitHub.com](https://github.com).

Repositories begin with the prefix `wt25`

- On lab computer, **sign in** to the GitHub [Open GIScience organization][https://github.com/opengisci]
- Confirm that you can see a repository named `wt25_...` where `...` is your GitHub user name
- Open the repository and copy the web address (e.g. `https://github.com/opengisci/wt25_...`)

Create an RStudio project with the GitHub repository on a lab computer

- Use default 64 bit version of R
- File -> New Project
- Version Control
- Git
- Repository URL: paste the web address of your `wt25_` repository
- Project directory name: use the default
- Create project as a subdirectory of: **browse** to your local `documents` folder. *Do not* store the project inside of any other project/repository or inside of any syncing folder (e.g. OneDrive, Google Drive, Icloud)
- Sign into GitHub when prompted using your browser

## Practice Using the Repository

- From the Files pane, open the README.md file
- Edit line 3 to use your own name
- Save the file
- In the Git panel, check the README.md file to **stage** it
- **Commit** the change with a message: `personalized my name`
- **Push** the commit to GitHub.com
- View the Readme file on GitHub.com to see the change (you may need to Refresh the browser)
- View the **Commits** history to see how this repository has been changed over time, one commit at a time
- View the most recent commit details to see a *diff* of the changes in that commit

## Set up the Repository on your Personal Computer

- Follow a similar process to set up the repository on your personal computer
- This will require having [Git downloaded and installed](https://git-scm.com/downloads)
- Create a `scripts` folder inside your repository
- Copy your notes (hopefully in R script format) from lecture into the `scripts` folder
- **Commit** and **Push** the changes
- Return to the lab computer and **Pull** the changes into the lab computer

## RMarkdown

- RMarkdown [rmarkdown.rstudio.com/](https://rmarkdown.rstudio.com/)

The morning lectures will provide both working R code vignettes to solve specific problems *and* explanations about the context/purpose of the code, how it works, and how to use it.
The best way to keep track of what you're learning is with **computational notebooks** to interweave narrative explanations and notes with working code blocks and outputs. 
In R, computational notebooks are **Rmarkdown** files.  
To maximize the legitiblity and usefulness of your class notes and in-class assignments, you are expected to create daily RMarkdown documents toward your participation grade.  
These will be due at **12:00 noon EST on Friday** each week, by committing them to your `wt25` GitHub repository.

### Create an RMarkdown document

- Go to File -> New File -> R Markdown 
- Update packages as prompted
- Enter a title for the first lecture, and your name as Author
- Use the default type (*document*) and format (*HTML* webpage)
- Go to Run -> Run All to see how RMarkdown works
  - R code is written inside code chunks blocked off by three backtics
  - Everything else is `Markdown`, a streamlined language for writing with simple formatting options
  - The default document contains three code blocks: one with default settings to include code in ouput, one to load data on car speed and distance required to stop, and one to graph the temperature and vapor pressure of Mercury 
  - Code blocks can be run one at a time with ctrl+shift+enter or the Green play button
  - Create new blocks with ctrl+alt+i or Code -> Insert Chunk or by typing out the code for a new chunk
  
  ```md  
  ```{r}
  ... your code here ...
  ```
  ```

- Markdown looks different, but it's really easy: check out this [10 minute tutorial](https://commonmark.org/help/tutorial)
- Rmarkdown Style:
  - Put every sentence on a new line
  - Leave a blank line in between each code block, heading, paragraph, or other element (e.g. table, blockquote, etc.) 

## Assets

- [ggplot2]({{site.baseurl}}/assets/ggplot2.pdf)
- [markdown]({{site.baseurl}}/assets/rmarkdown.pdf)
- [rmarkdown]({{site.baseurl}}/assets/rmarkdown.pdf)

