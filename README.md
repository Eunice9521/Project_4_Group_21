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
  We created four Natural Language Processing models and picked the SVM as our final model. 
  
  ![Final model](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/73389051-c499-4c2d-955b-b558500cdb0a)
  
  This is evident in the confusion matrix below after running our model prediction.

![New Confusion Matrix](https://github.com/Eunice9521/Project_4_Group_21/assets/133338843/b136cf35-e360-4980-b429-18eba5d47b4c)

  
  ## Conclusion
  
1. Brand Sentiment Impact: Key words in positive and negative word clouds are vital indicators, influencing customer loyalty and reviews.

2. Product Sentiment Analysis:

a) Apple Product:

Negative: 7.8%, Neutral: 60.6%, Positive: 31.6%

b) Google Product:

Negative: 5.4%, Neutral: 70.2%, Positive: 24.4%

c) Unknown Product:

Negative: 0.1%, Neutral: 98.3%, Positive: 1.6%

3. Market Research Insights: Varied sentiments for different products, e.g., more positive tweets for Apple, offer strategic guidance for SXSW.

4. Model Performance Overview: Post natural language processing, our model achieves 68.68% accuracy, excelling in neutral emotion recognition. Adjustments are needed for improved handling of negative and positive emotions and serves as a robust foundation for further refinement.
  
  ## Recommendation
  
1. Wordcloud Analysis: Utilize word clouds to compare frequently used words and identify those specifically associated with positive or negative sentiments. This approach can assist SXSW in flagging tweets containing these distinct words for sentiment identification.

2. Augmenting Dataset for Imbalance: Address the class imbalance by collecting more tweets labeled as positive or negative. Increasing the training data for these sentiments can enhance the model's accuracy and improve sentiment categorization.

3. Refining Stopwords and Tokenization: Identify and remove additional SXSW-specific stopwords to refine tokenization. This process aims to focus on words with more semantic value, contributing to a more accurate sentiment analysis.

4. Hyperparameter Tuning: Explore hyperparameter tuning for the SVM model and other potential algorithms. Adjusting parameters can optimize the model's performance, making it more adept at distinguishing between various emotional sentiments.

These strategies collectively contribute to a comprehensive approach for improving sentiment analysis, addressing challenges, and enhancing the model's effectiveness in capturing nuanced emotions related to SXSW.

## Next Steps
1. Exploring sentiments for specific products.
   Diving into which products are tweeted about favorably vs which ones are not. As we have already noticed, Apple has many more favorable tweets than Google does. This could help SXSW know which vendors are worth inviting/promoting.
   
3. Part of speech tagging for accurate lemmatization.
   Currently, our lemmatization is only functioning for nouns, not for verbs (ex: 'calling' is not lemmatized to 'call'). By instituting part of speech tagging to identify verbs and then lemmatize them could help our model's performance.
