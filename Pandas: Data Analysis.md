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
:page_with_curl: [to_csv_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html)
# dtype
- dtype stands for data type, it tells you what kind of values are stored in a DataFrame column or a series.
- Each column in a Pandas DataFrame or a series has a specific datatype<ins>(dtype)</ins>, such as:
  - int64 --> integer values
  - float64 --> decimal values
  - object --> text/string values
  - bool --> boolean (True/False)
> car_sales.dtypes\
:page_with_curl: [dtype_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dtypes.html)
# index
- In Pandas, <ins>.index</ins> is an attribute that represents the row labels( or row indices) of a DataFrame or Series.
> car_sales.index\
:page_with_curl: [index_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.index.html)
- You can also customize the index.
# describe()
- The describe() method returns description of the data in the DataFrame.
> car_sales.describe()<br>
:page_with_curl: [describe()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.describe.html)

> [!NOTE]
> It only works for numeric column.
# info()
- Prints information about DataFrame.
> car_sales.info() <br>
:page_with_curl: [info()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.info.html)
# mean()
- Returns a series with the mean value of each column.
> car_prices = pd.Series([13000, 567777, 88854]) <br>
> car_prices.mean() <br>
:page_with_curl: [mean()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.mean.html)
# sum()
- Returns sum of all items in an iterable.
> car_sales["Doors"].sum()
# tail()
- The tail() method returns a specified number of last rows.
- The tail() method returns the last 5 rows if a number is not specified.
![tail()](https://media.geeksforgeeks.org/wp-content/uploads/20220217141655/pandastail.png)
> car_sales.tail() \
:page_with_curl:[tail()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tail.html)
# loc() and iloc()
:memo::pencil: [difference between two](https://www.geeksforgeeks.org/machine-learning/difference-between-loc-and-iloc-in-pandas-dataframe/)
# pd.crosstab()

In Pandas, <ins>pd.crosstab()</ins> is a very useful function used to compute a <ins>cross-tabulation</ins> -- basically, a frequency table that shows how two( or more) categorical variables are related. 

![pd.crosstab()](https://github.com/shruti041/Machine-learning/blob/main/pd.crosstab().png) \
:page_with_curl: [pd.crosstab()_document](https://pandas.pydata.org/docs/reference/api/pandas.crosstab.html)

# groupby()

Method allows you to group your data and execute functions on these groups.

> car_sales.groupby(["Make"]).mean(numeric_only=True)\
:page_with_curl: [groupby()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html)

<hr>

> car_sales_missing = pd.read_csv("Desktop/car-sales-missing-data.csv")

# fillna() method
- This method replaces the NULL values with a specified value.
- It returns a new DataFrame object unless the inplace parameter is set to **True**, in that case the fillna() method does the replacing in the original DataFrame instead.
- By default inplace is set to **False**; returns a copy where the replacing is done.
>car_sales_missing["Odometer"].fillna(car_sales_missing["Odometer"].mean(), inplace = True)\
:page_with_curl: [fillna()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.fillna.html)

> [!NOTE]
>**Syntax** <br>
>dataframe.fillna(value, method, axis, inplace, limit, downcast)

# dropna() method
- This method removes the rows that contains NULL values.
- It returns a new DataFrame object unless the inplace parameter is set to **True**, in that case the dropna() method does the removing in the original DataFrame instead.
- By default inplace is set to **False**; returns a copy where the removing is done.
>car_sales_missing.dropna(inplace = True)\
:page_with_curl: [dropna()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dropna.html)

> [!NOTE]
>**Syntax** <br>
>dataframe.dropna(axis, how, thresh, subset, inplace)

# drop() method
- It removes the specified row or column.
> car_sales_missing.drop("Total fuel used",axis = 1, inplace = True)  # axis = 1 means column\
:book: [drop()](https://www.w3schools.com/Python/pandas/ref_df_drop.asp)\
:page_with_curl: [drop()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html)

# sample() method
- It returns a specified number of random rows.
- Returns 1 row if a number is not specified.
>car_sales_missing.sample(frac = 0.5)   # 50% of data and it is a copy of DataFrame\
>car_sales_missing = car_sales_missing.sample(frac = 1)  # all data\
>car_sales_missing  # changes made to original DataFrame\
:page_with_curl: [sample()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sample.html)

# reset_index() method
- This method allows you to reset the index back to the default 0,1,2 etc indexes.
> car_sales_missing.reset_index(drop = True, inplace = True)\
:page_with_curl: [reset_index()_document](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reset_index.html)

> [!NOTE]
> **Syntax**\
> dataframe.reset_index(level, drop, inplace, col_level, col_fill)

> [!IMPORTANT]
> By default this method will keep the **"old"** indexes in a column named **"index"**, to avoid this, use the **drop** parameter.

# apply() method
- This method allows you to apply a function along one of the axis of the DataFrame, **default 0**, which is the index(row) axis.
> car_sales_missing["Odometer"] = car_sales_missing["Odometer"].apply(lambda x: x / 1.6)\
:page_with_curl: [apply()_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html)
