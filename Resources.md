---
layout: page
title: Resources
---

There are a lot of questions and answers on the internet. This page lists resources that I have found useful, so I thought you might find them useful too.

# Starting out with R

Step one: <a href="https://cran.r-project.org/">download R</a> to your appropriate system (Windows, Mac, and Linux).

Step two: <a href="">download RStudio</a>. Trust me, RStudio makes using R much much easier.

If you are having problems with getting R or RStudio, check out <a href="https://github.com/fawda123/swmp_installR/blob/master/R_install_guide.pdf">this guide</a>, from <a href="https://beckmw.wordpress.com/2014/09/28/back-to-square-one-r-and-rstudio-installation/"> this guy</a>. It covers installing R and RStudio in a little more detail.

# Learning and Troubleshooting with R

To learn R, you need to learn <a href="">how to get unstuck with R.</a>

To learn a new function or package head to:

- <a href="http://www.statmethods.net">Quick-R</a>, which provides nice quick description of functions and aother R-things.</li>


For all my other problems, I usually google the error code, or search at 
<a href="http://stackoverflow.com">StackOverflow</a>

I would also recommend checking out:

- RStudio's <a href="http://www.rstudio.com/resources/training/online-learning/#R">list of resources for learning R</a>, and</li>

- <a href="http://www3.nd.edu/~mclark19/projects.html">This blog post</a>, which describes learning R from a social sciences background

And also, [RSeek](http://rseek.org/) is basically a google search that filters by R related content.



# Learning Advanced R

Got a basic handle on R and are hankering for more? I recommend these two (free, online) books by Hadley Wickham:

- <a href="http://adv-r.had.co.nz">Advanced R Programming</a>

- <a href="http://r-pkgs.had.co.nz">R Packages</a>

There is also this new book which seems similar(ish) to Hadley's books:

- <a href="http://www.quantide.com/R/r-training/r-web-books/ramarro-r-for-developers">Ramarro</a> 

# Advanced R stuff: S3 Classes

S3 classes are this really awesome minimal class of functions that can be super handy in R. They are described nicely in Hadley's book, but I have also found these to be helpful:

- <a href="http://www.cyclismo.org/tutorial/R/s3Classes.html">This R Book</a>, which is also an entire book on R programming.

- <a href="http://abhishek-tiwari.com/hacking/class-and-objects-in-r-s3-style">This blog post</a>, which also has such a suave blog layout ... Just sayin'.

<a href="http://www.youtube.com/watch?v=VZkD7DXQ-fk&amp;feature=g-upl">This video by Dr. Andrew Robinson.</a> Slides are also available <a href="http://files.meetup.com/1685538/presentation.pdf">here.</a> Thanks to <a href="http://damjan.vukcevic.net">Damjan Vukcevic</a>) for this information.

# Data Visualisation

`ggplot`

If you are going to do a plot in R, it should be in ggplot. It takes about 5 minutes to get the hang of, and once you've got it down you can create plots that make sense, behave how you expect, look fantastic.

ggplot ollows a logical syntax adapted from the book "The Grammar of Graphics". It makes visualisation make sense. And there are lots of other packages that build upon it to make it more awesome, such as GGally.

So here are some ggplot resources:

- [This handout](http://www.ceb-institute.org/bbs/wp-content/uploads/2011/09/handout_ggplot2.pdf) provides an introduction to ggplot.
- [The ggplot index](http://docs.ggplot2.org/current/index.html) The ggplot index page is usually where I head to first off when I want to understand how to add and build upon my graphs.
- [The R Graphics Cookbook](http://www.cookbook-r.com/Graphs/) is also really nice.
- I also recently discovered the [ggplot2 wiki](https://github.com/hadley/ggplot2/wiki), which has some great case studies and examples.
- The [RStudio ggplot cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/05/ggplot2-cheatsheet.pdf) is also really nice. It sits pinned up on my desk.

# ggvis

ggvis is another great package which builds upon the structure of ggplot but it allows for more interactive, reactive, plot building. Examples can be found [here](http://ggvis.rstudio.com/0.1/quick-examples.html) [here](http://ggvis.rstudio.com/ggvis-basics.html), and [here](http://ggvis.rstudio.com/cookbook.html).

# Shiny

shiny is a really awesome way to enhance your R plotting, and turn them into 'apps' (although whether they are actually apps is questionable, in my opinion).

- [shiny](http://shiny.rstudio.com/tutorial) tutorial
- [shiny cheatsheet](http://shiny.rstudio.com/articles/cheatsheet.html)
- [super awesome example](http://shiny.rstudio.com/gallery) here


# Data Manipulation

- Use [dplyr](https://github.com/hadley/dplyr) to manipulate data in R. [Here is a helpful lesson](http://www.dataschool.io/dplyr-tutorial-for-faster-data-manipulation-in-r)
- Use [tidyr](https://github.com/hadley/tidyr) to melt data (new version of `reshape2`)
- Use [broom](https://github.com/dgrtwo/broom#broom-lets-tidy-up-a-bit) to create **tidy dataframes** of statistical models. [Here is a helpful lesson](http://127.0.0.1:22465/session/Rvig.15c681ac18b1d.html)

# Reproducible Reporting

Probably the coolest thing ever. `knitr` is this amazing package that allows the user to combine their code and document text, making research easier to reproduce, and it does this while looking slick and classy. The idea is essentially to let the human do the writing, and the computer handle displaying the results, so that reports can be easily constructed, and most importantly, reproduced easily.

Check out some really nice guides [here](http://rmarkdown.rstudio.com/) and [here](http://rmarkdown.rstudio.com/html_document_format.html), and from the awesome dude who created knitr [here](http://yihui.name/knitr/).

You can also augment your rmarkdown documents with [templates](http://rmarkdown.rstudio.com/developer_document_templates.html). For example -  [rticles](https://github.com/rstudio/rticles) which is an r package that adds loads of rmarkdown templates. Currently, there are templates for the R Journal, the UseR Conference, Journal of Statistical Software, PLoS Computational Biology, and more!


# Learning R and Statistics

If you want to learn statistics using R, check out [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos) containing 15 hours of an applied R statistics course from Stanford. They also have an [excellent (and free!) book](http://www-bcf.usc.edu/~gareth/ISL/).

# Decision Trees

I use decision trees a lot in R, and I even [wrote a little package](https://github.com/tierneyn/neato) that helps take care of some common tasks in interrogating decision trees. Here are a list of resources that I recommend using to learn about them:

- [This book from James et al](http://www-bcf.usc.edu/~gareth/ISL/ISLR%20First%20Printing.pdf) - chapter 8 specifically refers to decision trees. They've also made the book free! Also [their videos](https://www.youtube.com/playlist?list=PL5-da3qGB5IB23TLuA8ZgVGC8hV8ZAdGh) on decision trees are very useful. You can find a comprehensive list of all their videos and material at [this website](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos)	

- This [book chapter](http://mason.gmu.edu/~csutton/vt6.pdf) from the Handbook of Statistics is broad and general.

- This [page](http://architects.dzone.com/articles/regression-tree-using-gini%E2%80%99s) helps explain regression trees. Their [gif](http://f.hypotheses.org/wp-content/blogs.dir/253/files/2013/01/gini-x1x2-x1-b.gif) demonstrating how decision trees choose splitting values is also really helpful.

- [This video on](http://www.statsoft.com/Textbook/Boosting-Trees-Regression-Classification) introduction to boosting trees for regression and classification by statsoft.

# STATA Related Resources

STATA do a great job of explaining multilevel and hierarchical models on their blog. I found these two blogs and video really helpful:

- [Blog part 1](http://blog.stata.com/2013/02/04/multilevel-linear-models-in-stata-part-1-components-of-variance/)

- [Blog part 2](http://blog.stata.com/tag/multilevel-models/)

-  [Video](https://www.youtube.com/watch?v=rUWT_EWV6QI)

# Typography

Just as it is important to have strong data visualisation skills, it is important to understand what makes a good looking document, poster, business card, and whatnot. To this end, you should read [typography in ten minutes](http://practicaltypography.com/typography-in-ten-minutes.html), and the [summary of key rules of typography](http://practicaltypography.com/summary-of-key-rules.html). One day I will purchase some fonts to pay him back.

<!-- # Blogs I like 

Of course, there is [r-bloggers]()
 -->
