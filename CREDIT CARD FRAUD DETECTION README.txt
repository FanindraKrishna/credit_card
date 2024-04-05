                                                                                                  
                                                      
                                                     PROJECT NAME :- Credit card Fraud detection 


ABOUT THE PROJECT :- 
HELLO SIR, 
This is a brief description of how i done and  implemented various fuctions of python and use supervised and unsupervised learning of machine learning by me 
 so in This project focuses on detecting credit card fraud using a dataset provided in a CSV file. The code begins by importing necessary libraries such as NumPy, Pandas, Seaborn, and Matplotlib for data manipulation and visualization. It also imports modules from scikit-learn for building machine learning models.

The dataset is loaded into a Pandas DataFrame using `pd.read_csv()`, and its basic properties are explored using methods like `df.head()`, `df.shape`, `df.describe()`, `df.dtypes`, `df.isnull().sum()`, and `df.duplicated().sum()`. Any duplicate rows are dropped using `df.drop_duplicates()`.

To identify outliers, the code defines a function `iqr_outlier_bounds()` that calculates the lower and upper bounds based on the interquartile range (IQR) outlier detection method. Another function `remove_iqr_outliers()` is defined to remove outliers from a specified column using the IQR bounds.

After defining these functions, the code applies outlier removal to the numerical columns of the DataFrame, excluding the 'Amount' column. It uses a loop to iterate over the columns, applying the outlier removal function using `remove_iqr_outliers()`. The modified DataFrame is stored back in `df`.

Next, the code visualizes the data distribution and outliers using box plots created with `sns.boxplot()`. Additionally, a count plot is generated to visualize the class distribution using `sns.countplot()`.

To address the class imbalance issue, the code balances the classes by undersampling the majority class (legitimate transactions) and combining it with the fraud transactions. The modified dataset is stored in `df_new`, and the class distribution is visualized again.

The code then splits the data into training and testing sets using `train_test_split()`. Four classification models (Logistic Regression, Decision Tree, Random Forest, and K-Nearest Neighbors) are imported from scikit-learn. The Logistic Regression model is trained on the training set using `model_1.fit()`, and its accuracy is evaluated using `model_1.score()`.

Overall, this project focuses on exploring and preprocessing the credit card fraud dataset, performing outlier removal, visualizing data distribution and class balance, and training a Logistic Regression model for fraud detection.
