House Price Prediction and Classification

Overview

This project focuses on predicting house prices and classifying them based on their prices using a dataset containing various features such as bedrooms, space, lot size, tax, bathroom count, garage size, and condition. The main goals are to build a linear regression model for price prediction and a classification model to categorize houses based on their price relative to the median.

Dataset
The dataset (realest.csv) contains information about various houses and their attributes, including:

Price: Sale price of the house.
Bedroom: Number of bedrooms.
Space: Size of the house in square feet.
Room: Total number of rooms.
Lot: Size of the lot.
Tax: Annual property tax.
Bathroom: Number of bathrooms.
Garage: Number of garages.
Condition: Condition rating of the house.

Code Explanation
Importing Libraries:

We use pandas for data manipulation and sklearn for building regression and classification models.

Loading the Data:

The dataset is loaded into a pandas DataFrame, and we inspect the first few rows and the data structure.

Data Cleaning:

We calculate the average values for columns with missing data (Space, Lot, and Tax) and fill those missing values with the computed averages.
We then drop any remaining rows with null values, ensuring our data is clean for analysis.

Linear Regression Model:

We separate the features and target variable (Price), split the dataset into training and testing sets, and train a linear regression model.
After training, we make predictions and evaluate the model using Mean Squared Error (MSE) and R-squared metrics.

Classification Model:

We calculate the median house price and create a new binary target variable (price_category), where houses priced above or equal to the median are categorized as 1 and those below as 0.
We build a Random Forest Classifier model to predict the price_category, evaluate its performance, and display accuracy and a classification report.

Results
Linear Regression:

Mean Squared Error: 65.67
R-squared: 0.65
Classification Model:

Accuracy: 90.63%
Classification Report includes precision, recall, and F1-score for each class.

Conclusion

The project successfully demonstrates how to predict house prices and classify them based on their prices using regression and classification models. The high accuracy of the classification model indicates that the features in the dataset are effective in predicting price categories.