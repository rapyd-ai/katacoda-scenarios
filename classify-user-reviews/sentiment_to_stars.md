How do we turn our sentiment scores into a star rating?

The easiest approach is to define some static rules, that match a star rating to a certain condition.

For our tutorial we defined the rules for converting AWS sentiment scores to a 5-star scale as follows:

* 5 Stars if positive sentiment == 1.00
* 4 Stars if positive sentiment >= 0.65
* 1 Star if negative sentiment >= 0.95
* 2 Stars if negative sentiment >= 0.85
* 3 Stars for everythin else

To apply this rule set, just call the following function to your dataset and save the output as a new column:

```
sentiment_df['Stars'] = aws_sentiment_to_stars(sentiment_df)
sentiment_df.head()
```{{execute}}