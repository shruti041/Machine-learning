# Why Pandas?
- Simple to use
- Integrated with many other Data Science and Machine Learning Python tools
- Help you get your data ready for Machine Learning
>[User Guide](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#min)
# 2 main Datatypes in Pandas :
1. Series ( 1 - Dimensional )
   >series = pd.Series(["BMW","Toyota","Honda"])\
   >colours = pd.Series(["Red","Blue","White"])
2. DataFrame ( 2 - Dimensional )
   >car_data = pd.DataFrame({"Brand" : series, "Colours" : colours})
# ![pandas-anatomy-of-a-dataframe](https://github.com/shruti041/Machine-learning/blob/main/pandas-anatomy-of-a-dataframe.png)
> car_sales = pd.read_csv("Desktop/car-sales.csv")
# to_csv()
- It is a pandas function used to export data from a DataFrame to a CSV (Comma-Separated-Values) files.
- It is one of the most common ways to save your processed or cleaned data.
>car_sales.to_csv("exported-car-sales.csv")\
:envelope: [to_csv_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html)
# dtype
- dtype stands for data type, it tells you what kind of values are stored in a DataFrame column or a series.
- Each column in a Pandas DataFrame or a series has a specific datatype<ins>(dtype)</ins>, such as:
  - int64 --> integer values
  - float64 --> decimal values
  - object --> text/string values
  - bool --> boolean (True/False)
> car_sales.dtypes\
:envelope: [dtype_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dtypes.html)
# index
- In Pandas, <ins>.index</ins> is an attribute that represents the row labels( or row indices) of a DataFrame or Series.
> car_sales.index\
:envelope: [index_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.index.html)
- You can also customize the index.
# describe()
- The describe() method returns description of the data in the DataFrame.
> car_sales.describe()<br>
:envelope: [describe()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)

> [!NOTE]
> It only works for numeric column.
# info()
- Prints information about DataFrame.
> car_sales.info() <br>
:envelope: [info()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.info.html)
# mean()
- Returns a series with the mean value of each column.
> car_prices = pd.Series([13000, 567777, 88854]) <br>
> car_prices.mean() <br>
:envelope: [mean()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.mean.html)
# sum()
- Returns sum of all items in an iterable.
> car_sales["Doors"].sum()



