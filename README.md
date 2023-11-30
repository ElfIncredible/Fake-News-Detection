# Fake-News-Detection

The overall goal of the code is to demonstrate the process of training text classification models to differentiate between fake and true news articles and provide a way to manually test the models with new input.
1. Data Loading and Preprocessing:
- Loads two datasets containing fake and true news articles.
- Adds a 'class' column to distinguish between fake (0) and true (1) news.
- Removes the last 10 rows from each dataset for manual testing.
- Merges the datasets into a single DataFrame.

2. Text Processing:
- Defines a function (wordopt) to process text data by converting to lowercase, removing special characters, links, HTML tags, punctuation, and digits.
- Applies the text processing function to the 'text' column in the DataFrame.

3. Data Splitting:
- Splits the data into features (x) and target labels (y).
- Further splits the data into training and testing sets.

4. Text Vectorization:
- Uses TfidfVectorizer to convert text data into numerical vectors for both training and testing sets.

5. Model Training and Evaluation:
- Trains four different classification models: Logistic Regression, Decision Tree Classifier, Gradient Boosting Classifier, and Random Forest Classifier.
- Evaluates the models using classification reports, which include precision, recall, and F1-score.

6. Model Testing:
- Defines a function (manual_testing) to manually test news articles using the trained models.
- Takes a news article as input, processes it, and predicts its class using each model.
- Prints the predictions for each model.

7. User Input:
- Takes user input for a news article.
- Calls the manual_testing function to predict the class of the input news using the trained models.
