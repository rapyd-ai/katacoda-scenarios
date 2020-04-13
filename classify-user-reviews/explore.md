To get some intuition about your dataset, we will plot some basic properties of the data. One critical factor is the text length. Basically, a good rule of thumb is anything between 50 to 100 characters on average. The longer each text phrase gets, the less practical is it ot squeeze the sentiment into one score.

You can view a distribution of your text lenght per line using the utility function:

`plot_text_length(reviews_df['Review_Text'])`{{execute}}