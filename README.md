
# DisasterResponsePipelines

## Required Libraries

* nltk 3.3.0
* numpy 1.15.2
* pandas 0.23.4
* scikit-learn 0.20.0
* sqlalchemy 1.2.12

## Motivation

The project is based on a dataset provided by [Figure Eight](https://www.figure-eight.com/). This dataset contains messages which were exchanged during various disasters and the categories which each message belong to. 

A model has been trained using Natural Language Processing and other machine learning techniques. Hence, we are capable of classifying a message and identifying relevant categories.

Further, this project includes a very basic web app, where an emergency worker can input a new message and get classification results in several categories (i.e. to identify various categories a particular message belongs to). The web app also display some visualizations of the dataset from Figure Eight.

Below are a few screenshots of the web app.

![Web App Index Page](/images/a.png)
Format: ![Alt Text](url)

![Web App Message Classification](/images/b.png)
Format: ![Alt Text](url)

## Files

* ETL Pipeline Preparation.ipynb: Description for workspace/data/process_data.py
* ML Pipeline Preparation.ipynb: Description for workspace/model/train_classifier.py
* workspace/data/process_data.py: A data cleaning pipeline that:
  * Loads the messages and categories datasets
  * Merges the two datasets
  * Cleans the data
  * Stores it in a SQLite database
* workspace/model/train_classifier.py: A machine learning pipeline that:
  * Loads data from the SQLite database
  * Splits the dataset into training and test sets
  * Builds a text processing and machine learning pipeline
  * Trains and tunes a model using GridSearchCV
  * Outputs results on the test set
  * Exports the final model as a pickle file


## Acknowledgements

I wish to thank [Figure Eight](https://www.figure-eight.com/) for dataset, and thank [Udacity](https://udacity.com) for advice and review.
