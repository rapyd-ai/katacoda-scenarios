Let's our newly gained knowledge to generate the sentiment scores for our dataset. 

But wait! Before we process our entire dataset, it is good practise to start with a sample. 

Why? Because every sentence that we send to RAPYD.AI will count against our quota limit. Thus, we want to make sure that everything is running correctly, before we spend our quota.

Let's sample our data to 50 rows for testing. If you are confident and have enough quota left you can simply skip this step or increase the sampling size.

```
sample_size = 50
reviews_df = reviews_df.sample(sample_size).reset_index(drop=True)

```{{execute}}

Now, we will actually enrich our dataset with the sentiment scores by calling the following function:

```
sentiment_df = add_sentiment_score_columns(reviews_df, "AWS", "AUTO", account_id, token)
```{{execute}}

Depending on the amount of sentences that you chose, this might take a while. For our sample of 50 sentences, however, this should take only 1-2 seconds.

If we look at our newly created object sentiment_df, you will notice the new sentiment scores:

```
sentiment_df.head()
```{{execute}}

