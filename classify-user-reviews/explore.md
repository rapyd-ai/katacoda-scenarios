To get some intuition about your dataset, we will plot some basic properties of the data. 

One critical factor is the text length. Basically, a good rule of thumb is anything between 50 to 100 characters on average. 

The longer each text phrase gets, the less practical is it ot squeeze the sentiment into one score.

We can see the average length as well as the maximum length of our text reviews by executing the following code:

`text_summary_stats(reviews_df.Review_Text)`{{execute}}

Be careful with very long text sentences as the sentiment score for this tends to be inaccurate. 

If you want to analyse sentiment not on a sentence, but on a document level, there are special APIs for this.