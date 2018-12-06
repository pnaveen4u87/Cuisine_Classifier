# Cuisine Classifier using Text Mining

## Overview
Digital news articles has become part and parcel of our lives, heavily used by people to retrieve information, express opinions, judgement on any kind of topics. Utilizing the large scale BIG data from these platforms extensively benefits in performing Data Analysis  solutions.
The lack of system to classify and filter the set of food related articles makes it challenging for the users to find the desired articles. 

In this project, we have built a classifier model which will classify the food receipies into different cuisines types and whether it is vegetarian or non vegetarian recipe based on the ingredients used. 

we have also bulit a web interface to filter and view the classified results and also to act as a interface to navigate to the source food receipe article.


## Team Members
- Naveen kumar Palani
- Rama Anem
- Shanthakumar Subramanian


## Data
In this project we are classifying the food reciepe articles available in the [BBC Website](https://www.bbcgoodfood.com/recipes/category/cuisines).

For training the classifier model, we used the data set from [Kaggle](https://www.kaggle.com/c/whats-cooking/data).


## Technologies/Algorithm Used
- Python 3.7.0
- nltk
- scikit-learn
- SVM Classifier Algorithm
- Github for version control

## Implementation
- Downloaded the dataset from [Kaggle](https://www.kaggle.com/c/whats-cooking/data).
- The data is in Json format. Read and stored it in dictionary and convert it to dataframe in Python.
- Did the following feature selection steps
  - Removed the punctuation, digits, content inside parenthesis.
  - Converted everything to lower case 
  - Removed stop words.
  - Performed stemming using Porter Stemmer algorithm.
- Encoded Cuisine column and veg/nonveg column using Label Encoder of sklearn.
- Converted the ingredients column after feature selection into TF-IDF Matrix.
- Split the data into train and test data in 80:20 ratio.
- Used different machine learning algorithm to find the algorithm which is having high accurancy in classfying the test data.
- SVM algorithm performed better for the test data so used SVM algorithm to predict the food articles.
- Scrapped the news article from [BBC Website](https://www.bbcgoodfood.com/recipes/category/cuisines) in required format.
- Converted the ingredients column into TF-IDF matrix similar to the data used for training.
- Predicted the cuisine using the SVM model built using kaggle data set.
- Stored the result in CSV and used it as the source for our webpage to filter and display the result.

## How to Use


## Limitation
The webpage is a very simplified version as it's just a place to dilever the classification result and ideas. The key part of this project is the classification based on the text data and the web page is just a sample model of the real world scenario. The data used in this project is a small set. In real world as the data scales, the efficiency of the classification may vary.

