---
title: How I built my website
layout: post
comments: true
---

I've recently changed from Wordpress to Jekyll. In this post I try and succinctly describe how I did it.

But first - why change from wordpress to jekyll?

Basically, I found that after using a [Slack]() - a work-chat platform, I was posting chunks of R code that I use, and I thought it might be start posting them up as little RMarkdown chunks onto my website, hosted on wordpress.



I had seen some posts about using RMarkdown with wordpress, and Yihui (creator of knitr)[has a guide for it](http://yihui.name/knitr/demo/wordpress/) so I figured it couldn't be so bad. And it isn't too bad, really - the only short coming is that you need to post your images/figures onto imgur or dropbox...But it can be done [as seen nicely here](https://yihui.wordpress.com/). So I was going to do that...

...But in his post, Yihui says:

> Note you can write and preview the draft in RStudio until you are comfortable to publish it. Once it is published, it is not straightforward to modify it (although you can), and that is why you, as a cool hacker, should blog with Jekyll instead of WordPress. It is always easy to deal with plain text files. Once you have got PHP, MySQL, password, plugins, ... things get complicated quickly.

And I thought...Jekyll, eh? I had heard of Jekyll, but wasn't really sure what it was - but I knew that [Hadley Wickham's books](http://adv-r-had.co.nz) can been built using it, so I figured if Hadley Wickham was using it, and Yihui says it's good, I felt that I should look into using it.

I started reading about using jekyll with RMarkdown and found some fantastic guides from other folk on the internet. These guys saved me a lot of time, so I would recommend reading their posts about this:

- joshua lande
- 
- 
-

It turns out that it isn't too hard to make a site using jekyll. In fact, it is really easy, because GitHub will provide free hosting of one blog for you using [github pages](https://pages.github.com/). It took about 30 seconds to make an absolutely barebones website (literally all it said in stock font was "Hello World"). You can then make a fully awesome website using Jekyll. 

Jekyll basically allows you to write plain text posts and using some straightforward commands in the terminal like jekyll build and jekyll serve, it does all the hard work and builds the HTML code and everything needed to get the website to work.

Basically, GitHub hosts the website for you, and you can use Jekyll to build the website content. The whole website can be made public on GitHub, so people can see exactly how everything works, and the whole website is stored locally, so I know exactly how everything works. It seems like a compromise between learning how to code a website from absolute scratch, and using a content management system like wordpress.  And I have control. Sounds good.

So I followed the instructions and then wanted to make the website cool, so I downloaded the style "lanyon" from Poole - made by GitHub, and then produced this website: tierneyn.github.io

Step 1. Create a GitHub Account

Step 2. Create a github page - as per their instructions

Step 3. Download requirements for jekyll - link

Step 4. followed directions from this blog: http://www.sitepoint.com/set-jekyll-blog-5-minutes-poole/

Step 5. 

**customizations**

I had a look around at a bunch of different blogs about how to build stuff

**getting a disqus comment feed**

1. Go to disqus, create account (if you haven't already)

2. go to settings (gear icon in the top right), and clikc "add disqus to site"

3. go to "engage", and fill in your site name, etc.

4. choose your platform - choose "universal code"

5. copy the code from disqus, being sure to [follow their instructions](https://help.disqus.com/customer/en/portal/articles/2158629), to "Recommended) Edit the RECOMMENDED CONFIGURATION VARIABLES section using your CMS or platform's dynamic values. See our documentation to learn why defining identifier and url is important for preventing duplicate threads."

As Joshua Lande points out, this : "By setting up the code this way, I can enable commenting on a page-by-page basis. All I have to do is set "comments: True" in the YAML header of the post."

I then decided that I couldn't understand what disqus wanted me to do...so I copies Joshua Lande's text from his github repo, changed his name for mine, and continued on. Isn't that cool? Isn't that why GitHub is so awesome?

And then continues folowing Joshua's advice over disqus.

**adding google analytics**

I didn't really know what google analytics was. so I went to their homepage. http://www.google.com/analytics/

I found the link "sign up for analytics". Sounds good. follow the prompts. 

I left all the boxes ticked. Google has my soul...accepted the ts and cs. 

google then gives me a tracking code, with a nice box, saying: "this is your tracking code".

**changing the page header format**

I went to poole.css and changed:

```

```

into

```
```



After looking at [Nicole White's](https://github.com/nicolewhite/nicolewhite.github.io) `_config.yml` I saw that she had written 

```
markdown: redcarpet
redcarpet:
  extensions: ["tables"] 
```

I was initially using `kramdown` to render the markdown, but that messed up my RMarkdown formatting, so I switched back.

So here is my pasted table using `knitr::kable(head(iris))`

Check it out:


| Sepal.Length| Sepal.Width| Petal.Length| Petal.Width|Species |
|------------:|-----------:|------------:|-----------:|:-------|
|          5.1|         3.5|          1.4|         0.2|setosa  |
|          4.9|         3.0|          1.4|         0.2|setosa  |
|          4.7|         3.2|          1.3|         0.2|setosa  |
|          4.6|         3.1|          1.5|         0.2|setosa  |
|          5.0|         3.6|          1.4|         0.2|setosa  |
|          5.4|         3.9|          1.7|         0.4|setosa  |




# Getting jekyll to work with RMarkdown

This turned out to be a bit of a journey, so I figured it would be better as a separate post - you can it here: ... link
