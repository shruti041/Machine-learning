# What is Pandas?
![logo](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/500px-Pandas_logo.svg.png)
- Pandas is a Python library used for working with data sets.
- It has functions for analyzing, cleaning, exploring, and manipualting data.
- It was created by *Wes Mckinney* in **2008**.
> import pandas as pd
# Pandas Read CSV
![read_csv](https://datascienceparichay.com/wp-content/uploads/2020/10/pandas-read-csv-file-as-dataframe.png)
- A simple way to store big data sets is to use CSV files. (Comma Separated Files)
- CSV files contains plain text and is a well known format that can be read by everyone including Pandas.
- In our example we will using a CSV file called **heart-disease.csv**.
> df = pd.read_csv("heart-disease.csv")\
> [pandas read_csv](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html)
# Pandas Dataframe head() Method
![head()](https://media.geeksforgeeks.org/wp-content/uploads/20220217141329/pandashead.png)
- The head() method returns a specified number of rows, string from the top.
- The head() method returns the first 5 rows if a number is not specified.
> print(df.head())
# What is Matplotlib?
![logo](https://studyopedia.com/wp-content/uploads/2022/12/Matplotlib-featured-image-studyopedia.png)
- Matplotlib is a low level graph plotting library in python that serves as a visualization utility.
- It was created by *John D.Hunter*.
- It is open source and we can use it freely.
## Matplotlib Pyplot
![bar graph](https://www.w3schools.com/python/img_matplotlib_bars1.png)
- Most of the Matplotlib utilities lie under the pyplot submodule, and are usually imported under the plt alias:
> import matplotlib.pyplot as plt
# Steps in Machine Learning Project
![steps](https://github.com/shruti041/Machine-learning/blob/main/6-step-ml-framework.png)
