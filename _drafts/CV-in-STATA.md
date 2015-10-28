STATA is a statistics package that is sued all around the world - it's simple, fast, and powerful.

In my research, I use multi-level models.  These are great for cases when there are multiple groups that are organised in a hierarchy.  For example, if you are looking at test results for school children.  These children are in classes, and these classes are in schools, and these schools are in larger regions.  It is important to account for this nesting.



A simple, if crude, example of this is a Matryoshka Doll - one of those nested russian dolls:

[Photo of a Matryoshka Doll]

There are all these dolls, nested within one another.  Just looking at the largest layer - you would falsely say that it is just a doll.  You would not uncover this interesting information, hidden within.  The same applies for these schools - ignoring these levels of nesting could be hiding important differences both between and within regions or schools or classrooms.

So that's Multi-level models.

I've run a heap of these - trying to find the best way to represent our data.  I thin I've got a few models that are really good.  But one really important step from here is to evalaute how well our model predicts data.  You can do this by plotting the predicted values from the model against those observed.

This is like...



