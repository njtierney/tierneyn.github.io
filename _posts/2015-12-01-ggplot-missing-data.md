---
title: "ggplot your missing data"
layout: post
comments: true
categories:
- R
- Missing Data
- rbloggers
---


Visualising missing data is important when analysing a dataset. I wanted to make a plot of the presence/absence in a dataset. One package, [`Amelia`](https://cran.r-project.org/web/packages/Amelia/index.html) provides a function to do this, but I don't like the way it looks. So I made a ggplot version of what it did.

Let's make a dataset using the awesome [wakefield package](https://github.com/trinker/wakefield), and add random missingness.


```r
library(dplyr)
library(wakefield)
df <- 
  r_data_frame(
  n = 30,
  id,
  race,
  age,
  sex,
  hour,
  iq,
  height,
  died,
  Scoring = rnorm,
  Smoker = valid
  ) %>%
  r_na(prob=.4)
```

This is what the Amelia package produces by default:


```r
library(Amelia)

missmap(df)
```

![plot of chunk unnamed-chunk-2](/figure/source/2015-11-12-ggplot-missing-data/unnamed-chunk-2-1.png) 

And let's explore the missing data using my own ggplot function:


```r
# A function that plots missingness
# requires `reshape2`

library(reshape2)
library(ggplot2)

ggplot_missing <- function(x){
  
  x %>% 
    is.na %>%
    melt %>%
    ggplot(data = .,
           aes(x = Var2,
               y = Var1)) +
    geom_raster(aes(fill = value)) +
    scale_fill_grey(name = "",
                    labels = c("Present","Missing")) +
    theme_minimal() + 
    theme(axis.text.x  = element_text(angle=45, vjust=0.5)) + 
    labs(x = "Variables in Dataset",
         y = "Rows / observations")
}
```

Let's test it out 


```r
ggplot_missing(df)
```

![plot of chunk unnamed-chunk-4](/figure/source/2015-11-12-ggplot-missing-data/unnamed-chunk-4-1.png) 

It's much cleaner, and easier to interpret.

This function, and others, is available in the [neato package](https://github.com/tierneyn/neato), where I store a bunch of functions I think are neat.

Quick note - there used to be a function, `missing.pattern.plot` [that you can see here](http://www.inside-r.org/packages/cran/mi/docs/missing.pattern.plot) in the package `mi`. However, it doesn't appear to exist anymore. This is a shame, as it was a really nifty plot that clustered the groups of missingness. My friend and colleague, [Sam Clifford](http://samclifford.info/) heard me complaining about this and wrote some code that does just that - I shall share this soon, it will likely be added to the [`neato` repository](https://github.com/tierneyn/neato).

Thoughts? Write them below.
