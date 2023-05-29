## Overview
This project aims to analyze a collection of Telegram messages related to a specific topic (CTER). It consists of three main components: a crawler to gather the messages, a topic modeling module to extract topics from the messages and on the Twitter data, and a meta-analysis module to perform analyses on the other Twitter data that functions as input for the topic modelling.

## Files

### 1. Crawler (Word_specific_Telegram_Crawler.ipynb)
The `Word_specific_Telegram_Crawler.ipynb` file contains the code for crawling and scraping messages from the specified Telegram channel. It utilizes web scraping techniques to collect relevant data for analysis. The crawler implements features such as specifying channels and filtering criteria.

To run the notebook the config.ini file needs to be placed within the same folder as the notebook.
Furthermore, the word_list.csv needs to be placed within the same folder as the notebook.
In the config.ini file the phonenumber, username, api_hash and api_id need to be filled in.
After saving the config.ini file with your credentials, the notebook is ready to run.

To obtain the API ID and API hash for a Telegram application, you need to follow these steps:

1. Go to the Telegram website (https://telegram.org/) and log in to your account.
2. Click on the "My Apps" section, which is located under your profile picture on the right-hand side of the page.
3. Click on the "Create new application" button.
4. Fill in the requested information, such as the name and platform of your application, and provide a brief description of its purpose.
5. In the "Security" section, you will find the API ID and API hash that were generated for your application.

Package requirements:
latest version of numpy, scipy, hdbscan and bertopic.

### 2. Topic Modeling (Topic_model_tweets.ipynb)
The `Topic_model_tweets.ipynb` file is responsible for extracting topics from the collected messages and Twitter data. It employs natural language processing (NLP) techniques, such as tokenization, stemming, and term frequency-inverse document frequency (TF-IDF), to preprocess the textual data. The file uses the algorithms LDA, LSA and BERTopic to identify and generate topic clusters.

To run the notebook the tweets.csv, word_list.csv and topic_words.csv files need to be placed within the same folder as the notebook.

### 3. Metadata Analysis (DF_analysis_metadatav3.ipynb)
The `DF_analysis_metadatav3.ipynb` file performs an analysis on the metadata in the Twitter dataset to gain insights and draw conclusions. It includes statistical analysis, data preprocessing methods and visualization techniques to understand the data. The output of this analysis can provide valuable information about trends present in the Twitter data, which could potentially lead to new indicators for extremist content being uncovered.

To run the notebook the tweets.csv file needs to be placed in the same folder as the notebook. More documentation on this dataset can be found at https://www.kaggle.com/datasets/fifthtribe/how-isis-uses-twitter.

