# Task 1: Predict Amazon Next Day Closing Price

## 1. Introduction
This project aimed to predict the next day's closing price for Amazon stock price. The structured approach outlined below was followed to achieve this objective.

## 2. Ask Question
The analytics process always begins with a question to be answered. In this project, the question pertains to the closing price of Amazon. Specifically, the query is: "What is the Amazon closing price for the next day?"
## 3. Get Data
This step involves the process of locating and obtaining data that is relevant to the question, and then determining if there is enough data to complete the analysis. To proceed, acquire 10 years of Amazon data from Yahoo Finance.
## 4. Investigate Data
Data comes in many forms and from various sources. This step involves determining if the data is complete and contains the relevant information necessary for the analysis.
## 5. Prepare Data
This phase involves various tasks aimed at transforming the data into a format suitable for analysis and presentation, commonly known as "data cleaning." This process entails rectifying issues such as blank records or obvious errors in the dataset, ensuring that the data is prepared and ready for analysis.
In this project, the following steps were taken:
*	Checked the shape of the data to obtain an overview of the number of columns and rows in the dataset.
*	Verified the column names in the dataset to confirm if the data is suitable for answering the project question.
*	Checked for null values and found non present.
*	Checked for duplicates and determined that there were no duplicate rows.
*	Identified the unique values in the dataset.
*	Obtained data information to understand the structure and types of data present.
*	Generated a statistical summary to understand the distribution of numerical data.
*	Examined the data distribution and found that it was partially normally distributed.
*	Evaluated data skewness and observed positive skewness.
*	Detected outliers, particularly in the Volume column.
*	Handled outliers by utilizing winsorization for columns with high outlier values and logarithmic transformation for columns with small or no outliers.
  
These steps collectively ensure that the data is clean, organized, and ready for further analysis.
## 6. Analyze Data
This step involves visualization tasks aimed at gaining more insight from the data. It encompasses Exploratory Data Analysis (EDA), where patterns, correlations, and relationships are visualized to gain a deeper understanding of the data. Through visualization, we aim to uncover insights and trends that may not be immediately apparent from the raw data, allowing for more informed analysis and decision-making.
## 7. Preprocessing
To predict the closing price, the project will remove the closing price column, adjusted close, volume column. Additionally, add technical indicator and target column. Then, assess the relationship between the remaining attributes and the target column. Afterward, delete the Nan values in Target column. Furthermore, normalize and reshape the data, and finally, split it into training and testing sets.
## 8. Model Design
This step involves designing the structure of the model. The model comprises an input layer with three-dimensional input, an LSTM layer with 75 units, a dropout layer with a learning rate of 0.2, a dense (fully connected) layer with 1 unit, and an output layer.
## 9. Model Training
This phase involves training the model on the training dataset. The model is validated using mean square error. It is trained on the training dataset and validated on the testing data. To avoid overfitting and bias, shuffle is used to control the data selected for training. Additionally, a batch size of 32 is employed for each epoch (30 epochs in total).
## 10. Model Testing
In this phase, the model is evaluated. First, predictions are made, and a line chart is plotted to compare the predicted values against the actual values. Additionally, the training and validation losses are printed. Mean Square Error, Mean Absolute Error, and Coefficient of Determination are then utilized to evaluate the performance of the model.
11. Closing Price Prediction
In this phase, the next day closing price of Amazon is predicted, followed by visualization of the closing price on a line chart.
