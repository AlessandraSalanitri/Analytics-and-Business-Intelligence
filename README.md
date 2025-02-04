# Analytics-and-Business-Intelligence
Descriptive statistics, plotting and visualizations and predictions. 
Pandas, Matplotlib, sklearn, seaborn library used.


# ⦁	OVERVIEW

This report analyses then the Titanic dataset using Jupiter Notebook in Colab and, Tableau.. The analysis is divided into three files to simplify the readability. The three files are attached as objects in the appendices.
The first file, demonstrates the ability to retrieve specific information from the dataset using Pandas library, and descriptive statistics by filtering the data based on column names and data types. 
The second file, illustrates the process of pre-processing data for visualization using Pandas, Matplotlib, and Seaborn libraries.
The third file, uses correlation, linear regression, train, and test split tools to extrapolate further insight from the data.
Finally, Tableau is used to present visualizations that effectively communicate key insights derived from the Titanic dataset.



# DESCRIPTIVE STATISTICS - PANDAS

In the 1st file, descriptive statistics are used for acknowledging some general and some detailed information about the Titanic dataset used from Seaborn library.

 
“Pandas was imported as pd”, where pd is the short name indicating that the Pandas library is being called. 
Pandas stand for “Python Data Analysis Library”, it is an open-source Python library used for analysing, cleaning, exploring, and manipulating data. 
“math” is a basic math python library. 
“Numpy was imported as np”, where “np” is the short name indicating that the numpy library is being called. Numpy is an open-source Python library, used for numerical data in Python. 
“Matplotlib.pyplot” was imported as “plt”, where “plt” is the short name indicating that the matplotlib.pyplot library is being called.
Matplotlib is a Python library for create 2D graphs and plots by using Python syntax. 
The “pyplot” module provides features to control graph proprieties as title, axes, etc.
“Seaborn” library as “sns”, where “sns” stands for Seaborn. Seaborn is a Python library used for high-level statistical graphs.
Additionally, %matplotlib allows your graphs to be included in the notebook file, next to the code.
As an initial prompt, the info() method is used to provide a comprehensive overview of the dataset, including the total number of entries, data column names, the total number of columns, data types - indicating whether the data is categorical or numerical-, and the presence of null values. Null values represent missing data points and can be the cause of challenges in data analysis as it can change the results of the analysis based on unreliable data.
 
The head() method displays by default, the first 5 rows of the dataset.
The query in the code below requests specifically the first 10 rows of the dataset, this is accomplished by inserting the desired value inside the parenthesis.
This method offers a first basic insight into the data structure and initial observations. 
 
To displays one, two, or more specific columns allowing further exploration of specific data points, the code below is used. 
In this case, because it is not specified how many rows are being required, by default, the first 5 rows will be displayed.
                                     
The tail() method, displays by default the last 5 elements of the dataset.
In the code below, however, the query is specifically requiring the last 10 rows.
    
The loc[ ] method retrieves specific rows based on the index value provided inside the brackets. In this case, the query extracts data from rows 10 to 20, displaying a targeted view of the dataset.
    
The shape() method provides a concise representation of the dataset's dimensions, returning a tuple containing the number of rows and columns.
                                        
The .dtypes attribute explicitly specifies the data types of each column, enabling a clear understanding of the data's structure.
                                 
The .columns attribute retrieves the dataset's header information in the form of a Pandas Series. 
       
The list() function converts this series into a standard Python list for further manipulation.
 
The .describe() method generates comprehensive statistical summaries of the dataset, including:
A count of null values for each column,
Mean, standard deviation (std), minimum, and maximum values for numerical columns.

By specifying a column title within the brackets, the mean for a particular column can be isolated and displayed.
  
Additionally, formatted strings can be employed to limit the decimal places of float numbers using the xf format, where x represents the desired decimal precision as shown in below code lines. This ensures a better readability for stakeholders and decision maker.
 
The. select_dtypes() method enables the extraction of columns based on their data types. The exclude and include parameters allow for selective filtering, making it easier to isolate specific data subsets.
             

The mean() , also known as average, is generally used for statistics and data analysis. It summarizes the entire dataset with a number that represents the data’s centre point.  
                              
The mode() is the most frequent value stored within a column. 
It is the only average value that can have no value, one value or more than one value. 
One value because if none of the number are repeated, that column does not have a mode. More than one value because if there are two values in the same column to have the same frequency, both values are the mode. 
Mode is often used in sample. Sample is a dataset collected from a targeted population.
 
Median is the value in the exact middle of the data.
To calculate the median, the value in the column needs to be sorted from smallest to largest.
  
The standard deviation or std measures the variation or dispersion in a set of values in a single number. 
It helps to identify trends and assess data reliability.
 
Variance measure how far the outliers are spread far from the mean.
 
-“Skewness is a measurement of the distortion of symmetrical distribution or asymmetry in a data set.”-   Ref. 4th.
The distribution of the data is illustrated as a curve. When the data do not have a normal distribution and, the curve is skewed to the left side, this is called a negative skewness. When the curve is skewed to the right side it is called the positive skewness.
 

Overall, this first file demonstrates the versatility of Pandas for data manipulation and analysis. The ability to extract, filter, and summarize data effectively facilitates deeper insights into the Titanic dataset.

04 PANDAS- MATPLOTLIB - SEABORN
VISUALIZATION.

The initial step of the second file is importing all the libraries necessary to extrapolate the information required to create visualizations.

    
PRE-PROCESSING

For plotting and visualization, it is required that the dataset has only reliable and usable data, hence, all duplicates’ values, null values needs to be dropped. 
To present an understandable report to Stakeholders and decision maker, our data needs to be as clear as possible. In this dataset, for example, some titles are not clear or descriptive such as sibsp, parch, etc. In this analysis, columns titles are being renamed with descriptive title replacing for example “sibs” title with “siblings or spouse” title. 

Now, the dataset has only reliable, understandable and usable data and it is ready to be analysed through graphs.

Exploring the Titanic dataset reveals many valuable information about the tragic disaster happened. 
The insights revealed in dept from titanic dataset are displayed in an understandable manner thanks to different graphs following.

Count plot counts the number of observations in each category and displays it as a bar chart.
Illustrating the number of individuals who managed to survive. 
  
The first graph displays the title:” Survived and Not survived”, a label indicating the survived (x axis), while the other axis represents the count of individuals. 
The legend is displayed thanks to the voice “hue” which act to separate the visualization of not survivors in blue colour, and the survivors in orange colour.
The graph suggests that around 122 people survived, while around 59 people died in the ocean.

The next graph analyses the rate of survival between female and male individuals. 
It suggests that the proportion of 
female survived (82) is higher than 
males’ survival rate (41). 
The mortality rate for female is lower (7) compared to males (54). This could be related to “women and children first” policy during emergencies. Further information could be found analysing this variable in dept.

The next graph analyses the passenger class and the survival rate.
The graph shows an exponential difference of survival rate based on the class each passenger was traveling in. The first class displays a higher rate of survival, while the second- and third-class passengers had low to none rate of survival.
The commented line #plt.ylabel (‘count’), assign the title “count” to “y axis”, however, because the action of the command is to count, the world “count” is displayed by default.

The next graph analyses the “Travel Status of Passengers” considering either passengers were travelling alone or with families’ members displayed in a vertical bar chart.

In the next graph, the Age Distribution by Passenger Class is displayed using box plot. 
Box plot is used to display the minimum, the maximum, the median and outliers of the age variable among each passenger class. 
The graph helps to easy compare the tendency and potential outliers within each class and could help identify patterns or differences in age distribution.
Below graph shows the passengers travelling in first class had an average of 38 years old, with the minimum number being 1 year old and the maximum being 80 years old. The second-class passengers had an average of 30 years old, with the minimum age being 2 years old and the maximum being 58 years old. The third class passengers had an average of 25 years old, with the minimum age being 3 years old and the maximum of 42 years old.
 
The next graph shows the relationship between variable “age” and “variable” fare.
It is suggested a strong correlation between the two data points. 

The next graph displays the age distribution within classes using a line plot.
Line plot graph uses data points displaying a clear representation of trends and patterns. 

SKLEARN
TRAIN/TEST SPLIT  

In the third file, sklearn library is imported along Panda, Seaborn, Matplotlib and numpy. 
Sklearn is a Python library widely used to implements pre-processing, cross-validation, regression, visualization, and algorithms.
From “sklearn.model_selection” module , the function “train_test_split”, splits arrays into random train and test subsets to wrap input validation.
From “sklearn.linear_model” module, the class “LinearRegression”. This class is used to perform linear regression, a basic predictive analytics technique. This technique is illustrated within this report (PAGE 34).
From “sklearn.linear_metrics” module, the function “mean_squared_error”.
Mean square error (MSE) is a measure of how close a predicted value is to the actual value. 
The imported module “warnings” is part of the Python standard library. The “warnings.filterwarnings() line, sets up filters for warning messages. In this file, it sets the ‘ignore’ action, hence any warning messages occurring during the program’s execution will not be printed to the console. In real life, warning messages are helpful because alert the developer regarding issues that may affect the program.
 
The classes imported from scikit-learn, are used to preprocess: “adult, alone, gender, alive and town embarkation” columns which are originally categorical data. 
Sklearn preprocessing module “Label Encoder” class, convert categorical data into numerical data. “OneHotEncoder” class convert each categorical integer into one-hot encoded new binary columns. Sklearn compose module “ColumnTransformer” class, used to preprocess datasets with a mix of categorical and numerical values. It helps by applying different transformations to different subset of column types.  

“Le”, stands for label encoder. 

“Drop duplicates()” translate for each column, the categorical data into unique numerical values as 0 or 1. 
The “fit” method is used to fit each label encoder on the unique values of the corresponding categorical column. 
  
“Transform” convert the actual values in the categorical columns to their corresponding numerical labels and set the new columns with the current titles plus “enc”. 
 
The remainder is initialized with the “ohe” alias which stand for OneHotEncoder, the transformer will be applied in the “town_embarkation” column. The “passthrough” parameter indicates the column which have not been called for any transformation process should be kept as it is.
 
In the following code, a new Data Frame named “ins_titanic” is created using the transformed data. The “ct.get_feature_names_out” method, return the name of the transformed data. The “list(ins_titanic.columns)” convert the column names of “ins_titanic” to a list and prints the results of all the transformed data and the ones that was kept without transformation.
 
Now each value of “town_embarkation” now has its unique column and has a value of 1 for existing individual embarked from that specific town and, a value of 0 for a non-existing individual embarked from that specific town. 
 
Finally, the column titles in the “ins_titanic” dataset are being renamed as specified in the list and, reordered.
then, a new data frame “ins_titanic_2” is created with selected columns from the existing data frame “ins_titanic”. Object columns are being removed. 
The “pd.to_numeric” convert the column passed by the list, to numeric data types.

The info() and head() method displayed all columns types are either float or integer hence, numerical value.
 
The method “.corr()” calculate the correlation coefficients between each selected columns and store them in a new data frame named “df_corr”.
If the correlation coefficient is 1 or close to 1, indicate a good or strong correlation.
If the correlation coefficient is -1 or close to -1, indicate a negative or no correlation.
 
Displayed within the analysis is a heatmap, which provides a visual representation of the correlation matrix previously analysed. On the right-hand side of the map, the legend illustrates how the colour intensity indicates the strength of the correlation. This helps quickly identify relationship between the data. 


For training and testing purposes,
This line of code : “ ” select all rows and columns except the last one as X.
This line of code : “ ” select all rows and the last column as Y.
This line of code : “  ”  splits the dataset into training and testing. The result is stored into the variables : x_train, x_test, y_train, y_test. The random_state=54 sets a random seed for reproducibility and, test_size specifies how much of the data will be used for testing and how much for training. In this case, 30% (0.3) of the data will be used for testing and, 70% for training.

The “model” has learned the relationship between the feature x_train and the variable y_train based on the linear regression algorithm. This model can now be used to make predictions or evaluation on its performance on a testing set.
 
Subsequently, illustration on how to extract the intercept “a” and coefficient “b” from the LinearRegression model previously trained.
The “model.intercept” contain the intercept “a” in the LinearRegression model. It represents the predicted value.
a = model.intercept_
The coefficient “b” represents the change in the predicted value.
B = model.coef_

These metrics provide MSE (mean squared error), RMSE (square root of MSE), MAE (mean absolute error) and R-square, which measure the proportion of the variance in the predictable variable from the independent variable.

Minimum, maximum and the difference between, of the “fare” column is then calculated. 
This process can provide insight on the distribution of the “fare” within the dataset
 
Displayed at last is the model prediction.
The model takes as first argument the passenger class which can either be 1,2,3, the gender (0 for woman, 1 for man), the age, either the passenger will be traveling with siblings or spouse (insert number), either the passenger will travel with parent or children (insert numb), either the passenger will travel alone (0 for no, 1 for yes).
Once all the arguments have been inserting on the model, it will predict the price of the ticket for this passenger.
The first example takes a passenger requiring 1st class, woman, 20 years old, traveling with 3 passengers, 0 parents or children, not alone. The predicted fare for this passenger is: 122.73£
 
The next example takes the same details as the previous example, changing only the gender. The predicted fare for this passenger is: 107.20£
 
Then, it takes the details of a 40 years old, woman, in 1st class travelling alone. The predicted fare is: 66.21£
 
The next example takes the details of a 1st class passenger, male, 40 years old, traveling with a spouse or siblings, three children or parents, not alone. The predicted fare is: 166.26£
 
More examples are displayed below. Now, for every new passenger request, it is possible to use the model to generate a prediction for their ticket fare.

