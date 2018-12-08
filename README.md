# Cuisine Classifier using Text Mining

## Overview
Digital news articles have become part and parcel of our lives, heavily used by people to retrieve information, express opinions, judgement on any kind of topics. Utilizing the large-scale BIG data from these platforms extensively benefits in performing Data analysis solutions.
The lack of system to classify and filter the set of food related articles makes it challenging for the users to find the desired articles. 

In this project, we have built a classifier model which will classify the food recipes into different cuisines types and whether it is vegetarian or non-vegetarian recipe based on the ingredients used. 

we have also built a web interface to filter and view the classified results and to act as an interface to navigate to the source food recipe article.


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
- The data is in Json format. Read and stored it in dictionary and convert it to data frame in Python.
- Did the following feature selection steps using WordNetLemmatizer and regular expression
  - Removed the punctuation
  - Removed digits.
  - Removed content inside parenthesis.
- Used rules to add Veg, Non-Veg information to the train data.
- Removed stop words and converted the words to lowercase using TfidfVectorizer.
- Converted the ingredients column after feature selection into TF-IDF Matrix using TfidfVectorizer.
- Split the data into train and test data in 80:20 ratio.
- Used different machine learning algorithm to find the algorithm which is having high accuracy in classifying the test data.
- SVM algorithm performed better for the test data so used SVM algorithm to predict the food articles.
- Scrapped the news food article from [BBC Website](https://www.bbcgoodfood.com/recipes/category/cuisines) in required format.
- Converted the ingredients column into TF-IDF matrix like the data used for training.
- Predicted the cuisine using the SVM model built using kaggle data set.
- Stored the result in CSV and used it as the source for our webpage to filter and display the result.

## How to Use
- We have published all the required file in this GitHub repository.
- Fork the project to your GitHub Id, if you want to use the web to filter and view the result or you can down the repository and setup the folder in you machine
- If you download the repository and use the project, you will be able to see the results only in CSV and not in the web.
- This tool is developed using Python 3.7.
- To use the tool make sure you have python and Jupyter notebook installed your machine.
- The following are the folders/files used by the classifier model
  - #### Main Folder
    - Classifier.ipynb – Jupyter note book to run the classifier
    - OutPut.csv – CSV file where the results will be saved by the classifier
  - #### Main Folder / Data Folder
    - Data folder has 2 folders
      - Train folder which has the train data from Kaggle in json format
      - Test folder which has the test data from BBC website in csv format
- To run the classifier, open the classifier.ipynb in jupyter notebook
- If you want to provide new training data to the model, you can place the new training data in the train folder in json format like the one already available.
- Provide the ingredients for the recipes for which you want find the cuisine type in the csv file in test folder
- Using jupyter notebook run all the chunks of code using Run All option in the cell menu
- The classified results will be updated in output.csv
### User Interface
- UI is implemented to view the list of recipes, ingredients which are categorized by the function to cuisine type and meal type
- UI works as below
  - User selects cuisine type, After selecting specific cuisine type, list of recipes , ingredient lists and other attributes displayed in UI, Basically UI shows the output of the model in UI form, where the model/ function actually classified the ingredients to cuisine type and meal type
  - Similarly User can select meal type as well from UI, which will show the list described above

## Limitation
The webpage is a very simplified version as it's just a place to dilever the classification result and ideas. The key part of this project is the classification based on the text data and the web page is just a sample model of the real world scenario. The data used in this project is a small set. In real world as the data scales, the efficiency of the classification may vary.

