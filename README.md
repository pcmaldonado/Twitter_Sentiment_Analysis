# Twitter Sentiment Analysis :blue_heart: :bird:
A popular MMORPG, GW2, has recently released its third expansion. Using the Twitter API, through tweepy,
to collect data and BERT to estimate sentiment, we can get an idea of how has the game being received by the community.

# Data
The data was collected using Tweepy to connect to the Twitter API. More than 1,000 tweets were collected containing the hashtag '#GW2EOD' for Guild Wars 2, End of Dragons -the new release from the game developer ArenaNet.

### Use of:
Python version: 3.9.7
Packages: Tweepy, Pickle, NumPy, Pandas, Re, Transformers, TextBlob, Torch, WordCloud, Matplotlib

# Overview
* Collected data using Tweepy and the Twitter API
* Instantiated a BERT model, *"finetuned to sentiment analysis on product reviews that predicts the sentiment of the review as a number of stars (between 1 and 5)"* [source](https://huggingface.co/nlptown/bert-base-multilingual-uncased-sentiment)
* Cleaned the dataset using regex and the Re library
* Applied the model to the clean dataset to obtain the sentiment of each tweet
* Plotted cloud of words from negative tweets (sentiment = 1) & from positive tweets (sentiment = 5)
* Using TextBlob, got the subjectivity and the polarity of each tweet

# Analysis
We can see that the vast majority of tweets are positive regarding the new release:

![Sentiment Distribution](https://github.com/pcmaldonado/Twitter_Sentiment_Analysis/blob/main/sent_dist.png)

----

Among those who seem to appreciate the game we can see that they find the new game "fun", "amazing", and "beautiful".

![Positive Cloud of Words](https://github.com/pcmaldonado/Twitter_Sentiment_Analysis/blob/main/pos_word_cloud.png)

----

Whereas people who seem to have a lower sentiment towards the new release seem to have a problem with the  "meta" (probably the final "meta" event that is currently known for its difficulty), the "bugs" and probably the time that it takes to do some parts of the game as "hour" seems to be associated with negative tweets.

![Negative Cloud of Words](https://github.com/pcmaldonado/Twitter_Sentiment_Analysis/blob/main/neg_word_cloud.png)

----

Finally, tweets presenting a high sentiment towards the game seem relatively more subjective than those who are not so enchanted with the new expansion. 

Unsurprisngly, the higher the sentiment gets, the higher the polarity (positive view). More unexpected, tweets that seem to lowly score the game still have a positive, although close to zero, polarity, meaning that the statements shared are still somewhat positive, or at least not that negative.

![Subjectivity and Polarity](https://github.com/pcmaldonado/Twitter_Sentiment_Analysis/blob/main/sub_pol.png)


----

Overall, the game seems a success and the community seem to appreciate and enjoy the new release by ArenaNet.