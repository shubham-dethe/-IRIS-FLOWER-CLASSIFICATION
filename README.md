# -IRIS-FLOWER-CLASSIFICATION
A datascience project to classify the Iris Flower on basis of different criteria. The dataset contains measurements of various iris flowers, including their sepal length, sepal width, petal length, and petal width, as well as their corresponding species: setosa, versicolor, and virginica.


**01]** First we import the necessary libraries such as numpy,pandas,seaborn. Matplotlib is a plotting library for Python. The 'pyplot' module provides a MATLAB-like interface for creating plots and visualizations.

Then we imported specific modules and classes from the scikit-learn library (sklearn) for a classification task



![Oasis Intership](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/6832ed84-71c5-4448-b560-185951a595d1)


**02]** We loaded the Iris dataset into a DataFrame named df using Pandas and displayed the first few rows using the head() method. This is a common practice to quickly inspect the structure and content of the dataset.

![read csv](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/a0e8f26d-dbcc-4a0f-ad6d-51be3f06340b)

**03]** Drop the id column
![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/ca3f8178-3f80-48ed-9c3d-1b04c3cc00d7)

**4]** We select the numeric column the line of code selects only the numerical columns from the DataFrame df. The select_dtypes method allows you to filter columns based on their data types.
The second line calculates the correlation matrix for the numerical columns selected in the previous step. The corr() method computes pairwise correlation of columns, excluding NA/null values. 

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/6548dba7-ef97-433a-b7ca-8dc86eddbcb6)

**5]** The code visualizes the correlation matrix using a heatmap, a common way to represent correlations between numerical variables.

**plt.figure(figsize=(10,5))**: This line creates a new figure for the heatmap with a specific size of 10 inches in width and 5 inches in height. This helps adjust the aspect ratio and make the heatmap more readable.

**sns.heatmap(correlation_matrix, annot=True, cmap='RdYlGn')**: This line creates the heatmap using Seaborn's heatmap function. It takes the correlation matrix (correlation_matrix) as input. The annot=True parameter adds numerical annotations to each cell of the heatmap, displaying the correlation coefficient value. The cmap='RdYlGn' parameter specifies the color map to use for the heatmap. Here, 'RdYlGn' represents the Red-Yellow-Green color palette.

**plt.title("Correlation of Iris dataset")**: This line sets the title of the heatmap to "Correlation of Iris dataset".

**plt.show()**: Finally, this line displays the heatmap.  Positive correlations are indicated by green shades, negative correlations by red shades, and no correlation by yellow shades. 

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/4ac8e04f-d155-4804-8a5a-ee8e2ffd1156)

**6]** Basic information of dataframe such as index, column name, non-null count and data type

df.shape[0]: This retrieves the number of rows in the DataFrame df.
df.shape[1]: This retrieves the number of columns in the DataFrame df.

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/2a4f1656-c546-4ce2-8719-8f21c2d093d2)

**7]** The code uses the describe() method in Pandas to generate descriptive statistics for the numerical columns in the DataFrame df.

It includes statistics such as the count, mean, standard deviation, minimum, 25th percentile (first quartile), median (50th percentile), 75th percentile (third quartile), and maximum values for each numerical column.

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/f37bf2d1-1266-459f-96b3-2c51a7eb5ed0)

**8]** Now counts the number of occurrences of each unique value in the 'Species' column of the DataFrame df. 

**df['Species']**: This selects the 'Species' column from the DataFrame df

**.value_counts()**: This method counts the frequency of each unique value in the selected column.

When you run df.nunique(), it returns a Series object where the index represents the column names, and the values represent the number of unique values in each column.

Also check the null values

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/80f712c0-76ef-4709-a20d-c1202183b4de)

**9]** Check and drop the duplicate

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/53c7a61d-ee6c-4dd8-92ad-27a9d0c9f24f)


**10]** This code creates a boxplot visualization of the data in the DataFrame df, allowing you to visually identify outliers before handling them.Finally displays the Plot

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/053b59c1-255b-4817-9aa5-8cb3abb7b8cd)

**11]** This code snippet creates a pair plot, also known as a scatterplot matrix, using Seaborn's pairplot function. Let's break down the code:

**sns.pairplot(df, hue='Species', palette='Dark2', diag_kind='kde')**: This line generates the pair plot. 

Here's what each parameter does:

**df**: This specifies the DataFrame from which the data for the pair plot will be drawn.

**hue='Species'**: This parameter colors the data points according to the values in the 'Species' column, allowing you to visualize the relationship between variables for each species separately.

**palette='Dark2'**: This parameter sets the color palette to be used for coloring the different species. 'Dark2' is a predefined color palette in Seaborn.

**diag_kind='kde'**: This parameter specifies that kernel density estimates (KDEs) should be plotted along the diagonal instead of histograms, providing a smoother representation of the distribution of each variable.

**plt.show()**: This line displays the pair plot.

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/ceb41057-5677-4851-b5d5-461522abda0d)

**12]** Now the code will plot the KDE plot depicting the distribution of sepal width and sepal length

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/d0517f61-2569-401b-a05b-a7c1366fd37b)


**13]** Similarly for the petal width and length 

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/eeb4acef-aaee-425e-9fc0-03b3341f554e)

**14]** By separating your data into features (X) and target (y), you're preparing it for training a machine learning model. The features will be used to predict the target variable.

The next code splits the data into training and testing sets using the **train_test_split** function from scikit-learn.

This code snippet demonstrates the process of creating and training a logistic regression model using scikit-learn (**LogisticRegression**). After executing this code, the logistic regression model (clf) will be trained and ready to make predictions on new data.

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/77261ef9-0369-44d9-8026-afc4d756658e)

**15]** This code snippet makes predictions using the trained logistic regression model (clf) on the testing data (X_test). After executing this code, y_pred will contain the predicted labels for the testing data based on the logistic regression model's learned parameters.

Next evaluates the performance of the logistic regression model by computing the accuracy score on the testing data

The classification_report function from scikit-learn provides a comprehensive report 

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/02c00caa-8f3a-462e-a713-d16a46db1719)













