# -IRIS-FLOWER-CLASSIFICATION
A datascience project to classify the Iris Flower on basis of different criteria. The dataset contains measurements of various iris flowers, including their sepal length, sepal width, petal length, and petal width, as well as their corresponding species: setosa, versicolor, and virginica.


**01]** First we import the necessary libraries such as numpy,pandas,seaborn. Matplotlib is a plotting library for Python. The 'pyplot' module provides a MATLAB-like interface for creating plots and visualizations.

Then we imported specific modules and classes from the scikit-learn library (sklearn) for a classification task



![Oasis Intership](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/6832ed84-71c5-4448-b560-185951a595d1)


**02]** We loaded the Iris dataset into a DataFrame named df using Pandas and displayed the first few rows using the head() method. This is a common practice to quickly inspect the structure and content of the dataset.

![read csv](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/a0e8f26d-dbcc-4a0f-ad6d-51be3f06340b)

Drop the id column
![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/ca3f8178-3f80-48ed-9c3d-1b04c3cc00d7)

We select the numeric column the line of code selects only the numerical columns from the DataFrame df. The select_dtypes method allows you to filter columns based on their data types.
The second line calculates the correlation matrix for the numerical columns selected in the previous step. The corr() method computes pairwise correlation of columns, excluding NA/null values. 

![image](https://github.com/shubham-dethe/-IRIS-FLOWER-CLASSIFICATION/assets/131885305/6548dba7-ef97-433a-b7ca-8dc86eddbcb6)

