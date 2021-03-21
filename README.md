### Disaster Response Pipeline Project

### Table of contents 
1. [Installation](#installation)
2. [Project Motivation](#explanation)
3. [File Description](#files)
4. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

You should import pandas, numpy, nltk, flask, plotly, sklearn, sqlalchemy, pickle. The code should run with no issues using Python versions 3.*.

Instructions to run the project:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## Project Explanation <a name="explanation"></a>

In this project, you'll find a data set containing real messages that were sent during disaster events. A machine learning pipeline is able to categorize these events so that you can send the messages to an appropriate disaster relief agency.

This project includes a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data.

## File Description <a name="files"></a>

- app
| - template
| |- master.html  # main page of web app
| |- go.html  # classification result page of web app
|- run.py  # Flask file that runs app

- data
|- disaster_categories.csv  # data to process 
|- disaster_messages.csv  # data to process
|- process_data.py # ETL Pipeline
|- InsertDatabaseName.db   # database to save clean data to

- models
|- train_classifier.py # ML Pipeline
|- classifier.pkl  # saved model 

- README.md

## Licensing, Authors, and Acknowledgements <a name="licensing"></a>

Datasets used for this project were available to me by Udacity and Figure Eight in order to build the model.
