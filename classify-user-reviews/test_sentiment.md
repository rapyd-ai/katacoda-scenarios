Now that we checked our data, let's get some sentiment scores. 

We will try one sample sentence at first in order to get an idea of what we are getting from the AI as a Service.

To analyse a sentence using RAPYD.AI, you just have to define your Account_ID and Token. 

To see your Account ID and generate an access token, login to [https://my.rapyd.ai](https://my.rapyd.ai)

Define your credentials by assigning them to the variables account_id and token: 

```
account_id = 'your-account-id'
token = 'your-temporary-token'
```

Now, let's define some sample text. You can assign any text you like or use our sample text here:

```
text = "I am getting coverage drops."
```{{execute}}

All you have to do is call the function get_sentiment_score and provide the text to analyse, the backend provider, the language (Auto detect is default), your AcocuntID and your token:

```
get_sentiment_score(text, "AWS", "AUTO", account_id, token)
```{{execute}}

As you see, the output will be an array with - in this case - 4 different levels (positive, neutral, mixed, negative). 

The output format will vary depending on the AI provider you are choosing. 

You can easily switch AI providers by replacing the parameter with either GCP, AZURE or AWS!

```
get_sentiment_score(text, "GCP", "AUTO", account_id, token)
```{{execute}}