---
layout: page
title: Resources
---

There are a lot of questions and answers on the internet.  This page lists sites that have been useful to me in my research, and sites that will hopefully help others!

# 'R' Related Resources

First things first, download [Rstudio](http://www.rstudio.com) to use R.

Rstudio provides a nice environment for using R, and makes life easier for you. Trust me.

[This guy has also written a blog](http://beckmw.wordpress.com/2014/09/28/back-to-square-one-r-and-rstudio-installation) about his first experiences installing R and RStudio and may be helpful.

## Starting out with R

If you are just starting out, I recommend checking out RStudio's [list of resources for learning R](http://www.rstudio.com/resources/training/online-learning/#R) list of resources for learning R. [This blog post](http://www3.nd.edu/~mclark19/projects.html) describes learning R from a social sciences background 

If you want to **learn statistics** using R, check out [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos) containing 15 hours of an applied R statistics course from Stanford. They also have an [excellent (and free!) book](http://www-bcf.usc.edu/~gareth/ISL/).

## Using R packages

Whenever I want to learn a new function or package, or have a question in R I usually head to a few places:

[Quick-R](http://www.statmethods.net): This provides really nice quick description of functions (and most things) in R

[StackOverflow](http://stackoverflow.com): When you google an R problem, this is where you usually end up.

## More Advanced R things

### R programming

Two online books by Hadley Wickham describe:

- [Advanced R Programming](http://adv-r.had.co.nz)

- [R Packages](http://r-pkgs.had.co.nz)

There is also this new book which seems similar(ish) to Hadley's books:

- [Ramarro](http://www.quantide.com/R/r-training/r-web-books/ramarro-r-for-developers)

### S3 Classes

S3 classes are described in Hadley's book, but I also wanted to mention two other blogs that I have found to be helpful:

- [This R Book](http://www.cyclismo.org/tutorial/R/s3Classes.html) Which is also an entire book on R programming.

- [This blog post](http://abhishek-tiwari.com/hacking/class-and-objects-in-r-s3-style) This blog post</a>. Which has such a suave blog layout. Just sayin'.

- [This video by Andrew Robinson](http://www.youtube.com/watch?v=VZkD7DXQ-fk&amp;feature=g-upl) [slides](http://files.meetup.com/1685538/presentation.pdf). Thanks to [Damjan Vukcevic](http://damjan.vukcevic.net) for this information.

## Data Visualisation

### `ggplot`

If you are going to do a plot in R, it should be in ggplot. The standard graphics in base R have a _slight_ advantage in speed , but ggplot's `qplot` takes care of that.

My rule: if I spend more than 2 lines of code for a plot in base R, I will switch to ggplot. Actually, scrap that, I just use ggplot now. The only exception is when I use an S3 plot.`specific package` function.

OK, so why use ggplot? It follows a logical syntax adapted from the book "The Grammar of Graphics". It makes visualisation make sense. And there are lots of other packages that build upon it to make it more awesome, such as GGally.

So here are some ggplot resources:

- [This handout](http://www.ceb-institute.org/bbs/wp-content/uploads/2011/09/handout_ggplot2.pdf) provides an introduction to ggplot.
- [The ggplot index](http://docs.ggplot2.org/current/index.html) The ggplot index page is usually where I head to first off when I want to understand how to add and build upon my graphs.
- [The R Graphics Cookbook](http://www.cookbook-r.com/Graphs/) is also really nice.
- I also recently discovered the [ggplot2 wiki](https://github.com/hadley/ggplot2/wiki), which has some great case studies and examples.
- The [RStudio ggplot cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/05/ggplot2-cheatsheet.pdf) is also really nice. It sits pinned up on my desk.

### ggvis

ggvis is another great package which builds upon the structure of ggplot but it allows for more interactive, reactive, plot building. Examples can be found [here](http://ggvis.rstudio.com/0.1/quick-examples.html) [here](http://ggvis.rstudio.com/ggvis-basics.html), and [here](http://ggvis.rstudio.com/cookbook.html).

### Shiny

shiny is a really awesome way to enhance your R plotting, and turn them into 'apps' (although whether they are actually apps is questionable, in my opinion).

- [shiny](http://shiny.rstudio.com/tutorial) tutorial
- [shiny cheatsheet](http://shiny.rstudio.com/articles/cheatsheet.html)
- [super awesome example](http://shiny.rstudio.com/gallery) here

## Data Manipulation

- Use [dplyr](https://github.com/hadley/dplyr) to manipulate data in R. [Here is a helpful lesson](http://www.dataschool.io/dplyr-tutorial-for-faster-data-manipulation-in-r)
- Use [tidyr](https://github.com/hadley/tidyr) to melt data (new version of `reshape2`)
- Use [broom](https://github.com/dgrtwo/broom#broom-lets-tidy-up-a-bit) to create **tidy dataframes** of statistical models. [Here is a helpful lesson](http://127.0.0.1:22465/session/Rvig.15c681ac18b1d.html)

# Decision Trees

I use decision trees a lot in R, and I even [wrote a little package](https://github.com/tierneyn/neato) that helps take care of some common tasks in interrogating decision trees. Here are a list of resources that I recommend using to learn about them:

- [This bookd from James et al](http://www-bcf.usc.edu/~gareth/ISL/ISLR%20First%20Printing.pdf) - chapter 8 specifically refers to decision trees. They've also made the book free! Also [their videos](https://www.youtube.com/playlist?list=PL5-da3qGB5IB23TLuA8ZgVGC8hV8ZAdGh) on decision trees are very useful. You can find a comprehensive list of all their videos and material at [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos)

- This [book chapter](http://mason.gmu.edu/~csutton/vt6.pdf) from the Handbook of Statistics is broad and general.

- This [page](http://architects.dzone.com/articles/regression-tree-using-gini%E2%80%99s) helps explain regression trees. Their [gif](http://f.hypotheses.org/wp-content/blogs.dir/253/files/2013/01/gini-x1x2-x1-b.gif) demonstrating how decision trees choose splitting values is also really helpful.

- [This video on](http://www.statsoft.com/Textbook/Boosting-Trees-Regression-Classification) introduction to boosting trees for regression and classification by 

# Reproducible Reporting

This is one of my favorite things right now. `knitr` is this amazing package that allows the user to combine their code and document text, making research easier to reproduce, and it does this while looking slick and classy. The idea is essentially to let the human do the writing, and the computer handle displaying the results, so that reports can be easily constructed, and most importantly, reproduced easily.

Check out some really nice guides [here](http://rmarkdown.rstudio.com/) and [here](http://rmarkdown.rstudio.com/html_document_format.html), and from the awesome dude who invented knitr [here](http://yihui.name/knitr/).

# 'STATA' Related Resources

STATA do a great job of explaining multilevel and hierarchical models on their blog. I found these two blogs and video really helpful:

- [Blog part 1](http://blog.stata.com/2013/02/04/multilevel-linear-models-in-stata-part-1-components-of-variance/)
- [Blog part 2](http://blog.stata.com/tag/multilevel-models/)
- [Video](https://www.youtube.com/watch?v=rUWT_EWV6QI)