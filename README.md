# Project_4_Group_21

# Understanding South by SouthWest

![SXSW](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/0d9417b4-1ebf-49d5-a063-eee4ff427f6c)

 Group Members:
1. Karanja Gakio
2. Eunice Nduati
3. Jane Mwangi

## Business Understanding

The South by Southwest (SXSW) conference, a prominent annual event highlighting technological and creative industry advancements, is keen on improving attendee experiences in future editions. To achieve this, the company aims to analyze sentiment from historical tweets related to the event. 

## Business Problem
The primary business problem is the need for a reliable and accurate sentiment analysis model that can effectively determine the sentiment conveyed in tweets associated with SXSW. The analysis of historical tweets is crucial for gaining insights into the public perception of the conference and the brands featured during the event. Additionally, the company aims to implement real-time sentiment tracking during ongoing events to provide a timely gauge of their reception. Developing a robust sentiment analysis model is essential for making data-driven decisions to improve and optimize the overall attendee experience at SXSW.

## Data Understanding
Our analysis will utilize a dataset provided by CrowdFlower, comprising approximately 9,000 tweets associated with past SXSW events. This dataset includes three key components:

1.Text: The actual content of the tweet.

Product: This field specifies whether the tweet pertains to a product or brand from Apple or Google.

Sentiment: The sentiment expressed in the tweet is categorized into:

'Negative'
'Positive'
'No Emotion'
By leveraging this dataset, we aim to build a robust sentiment analysis model that can effectively interpret and categorize the emotional tone of tweets, thereby offering valuable insights for enhancing future SXSW events.

## Business Objectives
 #### To find out the most commonly used words in negative sentiments.
    We used WordCloud to show most commonly used words in negative sentiments
    
  ![Negative Emotion wordcloud](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/3f7566a8-1e7f-4a41-978f-655339db95d8)
 
 #### To identify the most commonly used words in positive sentiments.

 We used WordCloud to show most commonly used words in positive sentiments
    ![Positive emotion wordcloud](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/b4ce62cf-1deb-4a23-a958-f89e92bf52e5)
 
 #### Product sentiment analysis.
 We used Bargraph showing sentiment distribution per product
 
![Sentiment distribution per product](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/b481922c-7db9-41be-b5f9-16e17ba415d6)

 4. Market research.
 Diving into which products are tweeted about favorably vs which ones are not. As we have already noticed, Apple has many more favorable tweets than Google does. This could help SXSW know which vendors are worth inviting/promoting.

 ## Data Cleaning
 We loaded our dataset using pandas then cleaned our data by:
 1. Changing column names for easy reference.
 2. Handing missing values.
 3. Removing duplicate entries.
 
  ## Exploratory Data Analysis
  1. Overall sentiment distribution.
  2. Examining unique words and their frequency.
  3. Analyzing hashtags and mentions.
  
  ## Modeling
  We created three Natural Language Processing models and picked the second as our final model. Our model is currently not predicting that any tweets are negative. This is most likely because there were relatively so few negative tweets in our training and test sets. With so few tweets, our model could not accurately identify them. 
  ![Final model](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/73389051-c499-4c2d-955b-b558500cdb0a)
  
  This is evident in the confusion matrix below after running our model prediction.

  ![Confusion matrix](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/a51bbb93-0402-4992-a773-e272833363a3)

  
  ## Conclusion
  
1.  Looking closely, there are some words that We would expect to see in each word cloud. For example, 'great', 'awesome', and 'cool' in the positive word cloud and 'fail', 'headache', and 'fascist' in the negative word cloud. The sentiments surrounding a brand are one of the most important factors to consider for a good customer experience. This is also reflected in brand loyalty, where positive sentiments result in good reviews and recommendations, while negative sentiments increase customer churn rates. 
  
2.  Product sentiment analysis.
   
   a) Apple Product: Negative Emotion: 7.8% Neutral Emotion: 60.6% Positive Emotion: 31.6%

  b) Google Product: Negative Emotion: 5.4% Neutral Emotion: 70.2% Positive Emotion: 24.4%

  c) Unknown Product: Negative Emotion: 0.1% Neutral Emotion: 98.3% Positive Emotion: 1.6%
  
 3. Market Research
  Diving into which products are tweeted about favorably vs which ones are not. As we have already noticed, Apple has many more favorable tweets than Google does. This could help SXSW know which vendors are worth inviting/promoting.
  
  After our natural language processing, our model is performing at 60.8% on our testing set.

Although we would prefer a model that performs at a higher level, we were constricted by the dataset. The dataset our model trained on included a much higher level of 'No Emotion' (60.2%) tweets than 'Positive' or 'Negative' tweets combined (39.8%).
  
  ## Recommendation
  
 1. Working with the dataset that we currently have We would recommend using the wordclouds to compare commonly used words and pull out the ones that are specificly linked to positive or negative tweets. SXSW can then flag tweets with these words to identify sentiment.

2. We believe that by collecting more tweets that are identified as positive or negative and increasing the number of tweets our model trains on, We would have the information needed to make more accurate recommendations.

3. Identifying and removing more SXSW specific stopwords could distill our tokens to words that have a semantic value.

## Next Steps
1. Exploring sentiments for specific products.
   Diving into which products are tweeted about favorably vs which ones are not. As we have already noticed, Apple has many more favorable tweets than Google does. This could help SXSW know which vendors are worth inviting/promoting.
   
3. Part of speech tagging for accurate lemmatization.
   Currently, our lemmatization is only functioning for nouns, not for verbs (ex: 'calling' is not lemmatized to 'call'). By instituting part of speech tagging to identify verbs and then lemmatize them could help our model's performance.
