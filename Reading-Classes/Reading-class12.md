# Pandas
What kind of data does pandas handle?

I want to start using pandas

    import pandas as pd
To load the pandas package and start working with it, import the package. 
The community agreed alias for pandas is pd, so loading pandas as pd is assumed standard practice for 
all the pandas documentation.

## pandas data table representation
To manually store data in a table, create a DataFrame. When using a Python dictionary of lists, 
the dictionary keys will be used as column headers and the values in each list as columns of the DataFrame.

A DataFrame is a 2-dimensional data structure that can store data of different types (including characters, 
integers, floating point values, categorical data and more) in columns. 
It is similar to a spreadsheet, a SQL table or the data.frame in R.

The table has 3 columns, each of them with a column label. The column labels are respectively Name, Age and Sex.

The column Name consists of textual data with each value a string, the column Age are numbers and the column Sex
is textual data.


Python is open source. It’s great, but has the inherent problem of open source: 

many packages do (or try to do) 
the same thing. If you’re new to Python, it’s hard to know the best package for a specific task. 
You need someone who has experience to tell you. And I tell you today: there’s one package you absolutely need to 
learn for data science, and it’s called pandas.


And what’s fascinating with pandas is that many other packages are hidden in it. 
Pandas is a core package with additional features from a variety of other packages. 
And that’s great because you can work only using pandas.

pandas is like Excel in Python: it uses tables (namely DataFrame) and operates transformations on the data. 
But it can do a lot more.

The most elementary functions of pandas
## Reading data

     data = pd.read_csv('my_file.csv')


     data = pd.read_csv('my_file.csv', sep=';', encoding='latin-1', nrows=1000, skiprows=[2,5])
sep means separator. If you’re working with French data, csv separator in Excel is “;” so you need to explicit it. 
Encoding is set to “latin-1” to read French characters. nrows=1000 means reading the first 1000 rows. 
skiprows=[2,5] means you will remove the 2nd and 5th row when reading the file

The most usual functions: read_csv, read_excel
Some other great functions: 
read_clipboard (which I use way too often, copying data from Excel or from the web), read_sql

## Writing data
     data.to_csv('my_new_file.csv', index=None)

I usually don’t go for the other functions, like .to_excel, .to_json, .to_pickle since .to_csv does very well the job. 
And because csv is the most common way to save tables. 
There’s also the .to_clipboard if you’re like me an Excel maniac who wants to paste your results from Python to Excel.

## Checking the data
    data.shape 
Gives (#rows, #columns)

    data.describe()
Computes basic statistics

## Seeing the data

    data.head(3)
Print the first 3 rows of the data. Similarly to .head(), .tail() will look at the last rows of the data.

    data.loc[8]
Print the 8th row

    data.loc[8, 'column_1']
Print the value of the 8th row on “column_1”

    data.loc[range(4,6)]
Subset from row 4 to 6 (excluded)

