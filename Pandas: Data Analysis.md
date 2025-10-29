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
# to_csv()
- It is a pandas function used to export data from a DataFrame to a CSV (Comma-Separated-Values) files.
- It is one of the most common ways to save your processed or cleaned data.
>car_sales.to_csv("exported-car-sales.csv")
- [to_csv_document](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html)
