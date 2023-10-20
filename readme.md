# nexthope-nlp
Sentiment Analysis on data breach topic tweets.

## Goal
This project aims to conduct sentiment analysis of tweets related to terms "data breach" that hopefully will be useful for data breach detection.

## Dataset
We scraped the tweets and doing data cleansing (removing slang/punctuation, adding space, etc) in order to be able to get insight from it. Our datasets can be found in the [datasets](https://github.com/lilypon246/nexthope-nlp/tree/main/datasets) folder. We also used kamus to do the sentiment analysis.

## Approach
We've done two approaches of vectorizer: using CountVectorizer and TF-IDF. Comparing those two performance with chosen classification algorithms (CountVectorizer using `Random Forest`, `SVM` and TF-IDF using `Random Forest`, `SVM`, and `IndoBERT`), we got the best result came from IndoBERT. 
| Vectorizer Method | Model | Accuracy | F1 Score |
| -------- | -------  | -------- | -------  |
| CountVectorizer | Random Forest | 0.78 | 0.73 |
| CountVectorizer | SVM | 0.78 | 0.72 |
| TF-IDF | Random Forest | 0.74 | 0.67 |
| TF-IDF | SVM | 0.79 | 0.68 |
| TF-IDF | IndoBERT | 0.82 | 0.79 | 


## Further informations about files

| File Name | Description|
| -------- | -------  |
| databocorv2_part2 | raw data from scraping |
| Scraping_preprocessing_v2 | output of notebook v1 |
| colloquial-indonesian-lexicon.csv | indonesian slang words dictionary |
