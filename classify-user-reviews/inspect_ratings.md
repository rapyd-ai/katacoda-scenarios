Lets find out how well our conversion perfomed by looking at the distribution of our newly created star rating. 

The ground truth of the sample dataset contained a balance of good and bad reviews, so we should see a similar amount of 1 star reviews and 5 star reviews with something going on in between.

We can check how many sentences have been classified for each category by calling:

```
sentiment_df.Stars.value_counts()
```{{execute}}

Looks like a pretty good distribution! 

Another good feedback is given by looking at the star rating individually. 

For example, let's look at some 5 Star ratings:

```
sentiment_df.query("Stars == 5")
```{{execute}}

Or take a look at some rather mediocre reviews:

```
sentiment_df.query("Stars == 2 | Stars == 3")
```{{execute}}

Looking at your classified data will give you a good idea if your decision rules for the star ratings actually match the data, or if you need a bit more tweaking.