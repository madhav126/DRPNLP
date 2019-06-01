# Disaster Response Pipeline 
In this project, the Natural Language Processing will be used to process the data from disaster responses. 

This project is focused on analyzing data provided by Figure Eight. The data is about responses from the people after certain disasters or situations and the goal is to identify the trend in this messages and classify them in certain categories. 
The project is divided in 3 parts:
1)	ETL Pipeline
2)	Machine Learning Pipeline
3)	Web application which will classify the disaster responses.

# Files:
1.	process_data.py : ETL Pipeline In a Python script (Load datasets, Merge datasets, Clean the data, and Store the data in a SQLite database).
2.	train_classifier.py : Machine Learning Pipeline In a Python script (Load data from SQLite database, Splits data into training and test sets, Builds a text processing and machine learning pipeline, Trains and tunes a model using GridSearchCV, Outputs results on the test set, and Exports the final model as a pickle file).
3.	Run.py : Flask Web App (display visualization from the datasets, the app accept messages from users and returns classification results for 36 categories of disaster events).

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
