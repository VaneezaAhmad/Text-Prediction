# Predictive Text

## Business Understanding
There is a ton of Language modeling and Natural Language Processing work done in English and other popular languages. This project is generating the predictions of words in Urdu which is the national language of Pakistan and the is popular in South East Asia. This prediction model can be used in many ways such for creating a virtual assistant, for a search engines or keyboard predictive text or for chatbots. This can make typing easier and faster for Urdu keyboard users.

![alt text](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Images/image.webp)

## Data Gathering
Data was collected from https://www.kaggle.com/disisbig/urdu-wikipedia-articles. The author of the dataset had over 100,000 wikipedia articles in urdu. For this project only 1000 of those articles were used. There are total 147477 words in the dataset and 5778 unique words.

![alt text](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Images/wordcloud.png)

## Data Preparation
1. All the text from each article was combined into one text and stored in a new file using glob.
2. The text was separated into words using Spacy.
3. There were a lot of special character, numbers and English words that needed to be removed from the text in order to use them in the model.
4. Then the preprocessed words were divided into feature and variable, the first 3 words were the feature and the next word (4th word) the target.
5. Words were converted to bag of words for the model to understand.

## Modeling
For modeling of the word predictions, Multiple Recurrent Neural Networks was created. Keras Sequential model was used. First a simple model was created using one LSTM, one dense and one output layer. In order to increase the performance of the model, more LSTM layers, Dense Layers, Dropout Layers for regularization and output layer were added.

![Models](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Images/best.png)

## Evaluation
The top 5 predicted words from the best model were used to evaluate the performance. The Metric used to evaluate model is keras' top k categorical accuracy. The best model had an accuracy of over 90%. Predicting 3-4 out of 5 words correctly.
![prediction](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Images/prediction.png)

## Further Steps
1. Get more informal coversation data. 
2. Integrating into keyboards, chatbots, virtual assistants. 

## Repository Navigation
1. [Urdu_predictive_text](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Urdu_predictive_text.ipynb): Main technical notebook 
2. [Urdu-data](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/Urdu-data/data.txt): Data files
3. [Predictive_text](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/predictive_text.ipynb): English predictions notebook
4. [English-data](https://github.com/VaneezaAhmad/Text-Prediction/blob/main/English-data/wonderland.txt): English Data

## Presentation Link
[Presentation](https://docs.google.com/presentation/d/1yRDKk7GH60GliDWCCqYwnU2MjQ2-2iMeTHeyJNUe01k/edit#slide=id.ge5366def7b_0_0)