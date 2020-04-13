For this prototype, we will need a dataset with some user reviews. The data has to come as a csv file without header, where each line is one text review that we want to classify.

If you don't have a text file at hand, or if you want to look at a sample, you can just call the utility function:

`reviews_df = read_reviews()`{{execute}} 

To copy your file from a remote URL to this training machine, execute the following command and replace the url with your file accoringly:

```
quit()
wget -O "data/reviews.csv" "https://insert-your-url.here/
python3
```

To check if the import was successful, run:

`reviews_df.head()`{{execute}} 

This should print the first couple of text reviews.