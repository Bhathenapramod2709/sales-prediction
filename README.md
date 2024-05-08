# sales-prediction
sales_prediction_ Issue: This code attempts to solve the issue of predicting sales based on advertising costs across various media platforms (TV, radio, newspaper).


Steps in Analysis:

Importing Libraries: NumPy, Pandas, Matplotlib, Seaborn, and scikit-learn (for machine learning) are among the Python libraries that must be imported before the code may run.

Bring the Dataset in: 'Advertising.csv' is the dataset that the code reads into a Pandas DataFrame. It is likely that this collection includes statistics on advertising costs and related sales.
Comprehending Data:

The number of non-null entries and the data types of each column are among the details about the dataset that may be obtained with the data.info() command. For numerical columns, summary statistics are provided using the data.describe() command. The data types of each column are displayed using the data.dtypes command. The names of the dataset columns are shown using the data.columns command. Data Purification:


The code uses data to check for missing values.sum().isnull() and discovers nothing. Moreover, it counts the number of duplicate rows and looks for duplicates. The 'Unnamed: 0' column, which would have been an index column, is eliminated. Data Conversion:

A number of columns are transformed to integers, including "TV," "Radio," "Newspaper," and "Sales." Exploratory Data Analysis, or EDA:
For the expenses of "TV," "Radio," and "Newspaper," the code generates box plots to show the distribution and existence of outliers. When values in the 'Newspaper' column are more than or equal to 100, outliers are eliminated. Distribution plots are utilized for univariate analysis in the areas of "TV," "Radio," "Newspaper," and "Sales." A correlation heatmap is used in multivariate analysis to visualize the relationship between variables. Model Construction:

In order to create a machine learning model, data must be prepared. The goal variable (y) and features (x) make up the dataset. A second division of the data is into training and testing sets. StandardScaler is used to apply feature scaling to the data. The model of linear regression:
The scaled training data is used to design and train a linear regression model. Based on the scaled testing data, predictions are formed. It is built a DataFrame that compares expected sales ('pred') with actual sales ('y_test'). Actual sales compared to forecast sales are shown as a scatter plot. Assessment of the Model:

Several evaluation measures for the linear regression model are computed by the code: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared (R2) score In summary:


According to the code comments, the model's accuracy in forecasting sales based on advertising expenses was 81%.
