# British_Airway

This british airway website was the meaning source of our data (customers reviews), so 1st i scrapped the data through beatiful soup, and for 10 of pages i did the scraping.
Then i start with using the sentiment techniques to create the polaity for each sentence/review, after that i classifid the TextBlob polaritis depends on the following:
if num<0:
        return 'Negative'
    elif num >0:
        return 'Positive'
    else:
        return 'Neutral'.
for Vader method:

 if num >= 0.05:
        return 'Positive'
    elif num <= -0.05:
        return 'Negative'
    else:
        return 'Neutral'

after classification for each of the polarities i labelled them into 0 for Nigative, 1 for Positive and 2 for Neutral. 
Next step is vectorizing the sentences using bag of words. After that i splitted the data info training and test dataset for create predicting model depending on our vectorizer for the two
techniques Vader and TextBlob. Further, i sart modelling the datasets with MultiNominal classifier. Finally i evaluated our predicting model, the result for accuracy value comparing
was 0.7 for Vader, better than textblob accuracy value which was 0.6
