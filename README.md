# Statistics Meets Logistics

The [course](https://www.statistik.tu-dortmund.de/2791.html) and the [material](https://moodle.tu-dortmund.de/enrol/index.php?id=22199) provided by the lecturer are in German. The documentation is in English. This repository documents our preparation for the project and holds the project and its data.

# 📖 Description

In the course, students will learn about the application of statistical methods and basic machine learning procedures for the analysis of complex data in the field of logistics. This includes methods of descriptive statistics as well as various regression and classification procedures including neural networks. After the introduction of the methods, the students apply the acquired knowledge independently to work on logistical problems in various practical exercises. The software Python and relevant packages are used.

# 🌅 Background

In this section we setup the relevant systems for the project and provide additional material not directly tied to the project.

## Getting Started with Anaconda

- Anaconda curates data science packages for analysis, visualization and modelling (200+ packages)
- Conda package manager
    - install, remove, and update packages
    - automatically installs dependencies
    - install packages written in any language
    - no compiler needed
- Conda environments: keep multiple versions installed
    - think of them as separate Python installations
    - packages can be installed, upgraded and downgraded (using conda or pip)
    - directly from Anaconda Navigator
- base (root) environment is the default environment

Community, documenation and events:

[Anaconda | Open Source](https://www.anaconda.com/open-source)

[Anaconda Documentation - Anaconda documentation](https://docs.anaconda.com/)

[Anaconda | Events](https://www.anaconda.com/events?utm_medium=webinar&utm_source=anaconda&utm_campaign=intro-to-individual)

[Installing Python Packages from a Jupyter Notebook](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/)

## Jupyter Notebook

Version control with Git: 

[Reproducible Data Analysis in Jupyter, Part 3/10: Version Control with Git & GitHub](https://www.youtube.com/watch?v=J45NJ0pJXWQ)

Useful shortcuts in Jupyter notebook: 

[Jupyter Tips and Tricks](https://www.youtube.com/watch?v=2eCHD6f_phE&t=0s)

[My favorite Jupyter notebook shortcuts](https://www.youtube.com/watch?v=FW2BF6jbHBk)

## JupyterLab

[JupyterLab](https://github.com/jupyterlab/jupyterlab) is the next-gen user interface for Project Jupyter offering all the familiar building blocks of the classic Jupyter Notebook (notebook, terminal, text editor, file browser, rich outputs, etc.) in a flexible and powerful user interface. JupyterLab will eventually replace the classic Jupyter Notebook.

[Contributing to JupyterLab - JupyterLab 2.3.0a2 documentation](https://jupyterlab.readthedocs.io/en/stable/developer/contributing.html?highlight=virtual%20environment#installing-jupyterlab)

[How to add conda environment to jupyter lab](https://stackoverflow.com/questions/53004311/how-to-add-conda-environment-to-jupyter-lab)

## VS Code

Another alternative is VS Code. See [Documentation](https://code.visualstudio.com/docs/python/jupyter-support); note that to work with other languages such as Julia or R the [marketplace extension](https://code.visualstudio.com/docs/python/jupyter-support) has VS Code Insiders as a prerequisite. 

## Version Control with Git

Keep track of the history changes done to code > facilitate collaboration

[Version Control (Git)](https://missing.csail.mit.edu/2020/version-control/)

[gitignore.io](https://www.toptal.com/developers/gitignore)

## Basic Markdown

[Basic Syntax | Markdown Guide](https://www.markdownguide.org/basic-syntax/)

[adam-p/markdown-here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Virtual Environments

[Managing Environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

[Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

There are two options:

1. Import `requirements.txt` as Conda explicit specification file
2. Run the following command in the command prompt interface (Anaconda prompt or directly in the terminal):

`conda create --name <envName> jupyter==1.0.0 lxml==4.5.1 MarkupSafe==1.1.1 matplotlib==3.3.2 notebook==6.0.3 numpy==1.18.1 openpyxl==3.0.4 pandas==1.1.2 Pillow==7.2.0 scikit-learn==0.23.2 scipy==1.4.1 seaborn==0.11.0 SQLAlchemy==1.3.18`

or

`conda create --prefix ~/opt/anaconda3 jupyter==1.0.0 lxml==4.5.1 MarkupSafe==1.1.1 matplotlib==3.3.2 notebook==6.0.3 numpy==1.18.1 openpyxl==3.0.4 pandas==1.1.2 Pillow==7.2.0 scikit-learn==0.23.2 scipy==1.4.1 seaborn==0.11.0 SQLAlchemy==1.3.18`

## Setup the virtual environment

There are two options:

1. Import `requirements.txt` as Conda explicit specification file
2. Run the following command in the command prompt interface (Anaconda prompt or directly in the terminal): 

`conda create --prefix ./envs jupyter==1.0.0 lxml==4.5.1 MarkupSafe==1.1.1 matplotlib==3.3.2 notebook==6.0.3 numpy==1.18.1 openpyxl==3.0.4 pandas==1.1.2 Pillow==7.2.0 scikit-learn==0.23.2 scipy==1.4.1 seaborn==0.11.0 SQLAlchemy==1.3.18` 

## Activate the virtual environment

There are two options: 

1. On the Anaconda Navigator: Environments tab > choose the environment > open application on the environment
2. In the terminal: `conda active myEnv` (replace `myEnv` the name of your environment)

# 🐍 Python Crash Course

This is the section for the Python crash course. [Python documentation](https://docs.python.org/3/contents.html).

## Crash Course

If a variable is being highlighted by the IDE, this keyword is reserved for an object!

- String interpolation / [.format()](https://pyformat.info/) on string = a way to insert things into a string. More info on [format method](https://www.w3schools.com/python/ref_string_format.asp). See improved [String Formatting Syntax Guide](https://realpython.com/python-f-strings/).
- List = arrays in other languages. In Python a list can contain objects of different types. Lists can be nested (useful with 2D object, e.g. a matrix). Important function:
    - list(iterable) is a list constructor.
    - Append: Adds its argument as a single element to the end of a list. The length of the list increases by one
    - extend(): Iterates over its argument and adding each element to the list and extending the list. The length of the list increases by number of elements in it’s argument
    - There is distinct algebra defined for Lists, e.g. [1,2] * 2 = [1,2,1,2]
- Dictionaries = hash tables in other languages. Dictionaries do not retain any order! Important function: update([other])
- Truthy and Falsy values: Python treat the following values as False: `"", 0, 0.0, 0j, [], (), {}, False, None, instances which signal they are empty`
- Tuples are immutable
- Sets: unordered collection of unique elements
- Range `range(arg)`: iterate though elements of range 0, ... , arg or create a list with the elements of the range
- List comprehension: flatten loop to populate an empty list: `[f(i) for i in range(arg)]`
- Flatten conditional statements: `var = value1 if statement 1 else value2`
- Lambda expression / anonymous function: short function that are (usually) used only one time: `lambda input:output`. We use them along another outside function. To define a lambda expression remove `def` and `return` and write the function in one line
- Useful methods for strings:
    - st.lower()
    - st.upper()
    - [st.split()](https://www.youtube.com/watch?v=Sr3tOzYYWfQ): by default on white space and returns a list with the words in the string. Split string to iterate over words rather than characters.
    - [st.partition(separator)](https://www.youtube.com/watch?v=si-IpgT2Z2M): if separator is in string the method will return three strings contained in a tuple (first_substring, separator,remaining_su bstring) ([stack overflow](https://stackoverflow.com/questions/12572362/how-to-get-a-string-after-a-specific-substring)).
    - Other important ones:
        - strip()
        - replace()
        - join() and split()
        - translate()
- Useful methods for dictionaries:
    - dic.keys()
    - dic.items()
- Useful methods for lists:
    - myList.pop(arg): remove the item passed in the argument (by default it removes the last item) and assign it to a variable
    - in operator: i in myList
    - `:` in square brackets to show passed number of elements
- [Map, filter, and reduce](https://www.youtube.com/watch?v=hUes6y2b--0):
    - map(function, iterable): takes a function and a iterable object (set, list, tuple, or containers of any iterators). The output of the function is a map object. We can turn it into a list by passing the map to the list constructor
    - filter(statement, iterable): select subdata from data. It filters the data we do not need. The filter function will only return the data for which the statement / function is True
        - filter(None, data): filters out all values that are treated as false in a boolen setting. **Be careful** with 0, as they are treated as False in Python
    - reduce(): no longer a built in function. It can be found in the 'functools' module.

# 🤖 Machine Learning Pathway

General idea of a pathway of using Machine Learning and Data Science for useful applications, e.g. create a data report or product. We'll try to distinguish between Data Engineer, Data Analyst, Data Scientist, and Machine Learning Researcher. 

## Meta-Pathway

Real World > Problem to Solve or Question to Answer > Real World

Problem to Solve:

- How to fix or change X?
- Create: data products, e.g. mobile apps, services, websites, etc.

Question to Answer

- How does a change in X affect Y?
- Create: data analysis, e.g. reports, visualization, communications, etc.

## Pathway

Real World > Collect & Store Data <> **Data Analysis** > Machine learning models > Real World

C**ollect & Store Data** (Role: Data Engineer):

- Raw Data: data from physical sensors, surveys, simulation, experiments, data usage, etc.
- Process & Store Data: SQL database, CSV files, Excel files, cloud storage, etc.

**Data Analysis** (Role: Data Analyst or Data Scientist)

- **Clean & Organize Data**: reorganize data, dealing with missing data, restructure data, etc.
- Overlap with Collect & Store Data: reorganize data, dealing with missing data, restructure data, etc.
- **Exploratory Data Analysis**: statistical analysis (e.g. hypothesis test) and visualizations
- Create: report, visualization or communication > Answer question by understanding different trends and visualizations > Make  decision & Answer key questions

Machine Learning Models (Role: Data Scientist or Machine Learning Engineer)

- Supervised Learning: Predict a future outcome (based on labeled historical data)
- Unsupervised Learning: Discover hidden patterns in data
- Create: service, dashboard, application, etc > data product (predict future outcomes or gain insight on data) > Affect some change in the real world

# 🥧 NumPy

[NumPy](https://note.nkmk.me/en/python-numpy-ndarray-ndim-shape-size/#:~:text=len()%20is%20the%20built,only%20for%20one%2Ddimensional%20arrays.) is a Python library. Almost every data science library is built using NumPy.

Goals: 

- Undestand NumPy
- Create arrays with NumPy
- Retrieve info from a NumPy array through slicing and indexing
- Learn basic NumPy operations

Definition: 

- Python library for creating n-dimensional arrays
- Ability to broadcast functions
- Build-in linear algebra, statistical distributions, trigonometric, and random number capabilities

Motivation: 

- NumPy arrays are more efficient than Python lists
- Broadcasting capabilities useful for quickly applying functions to data set

## Array

Create by: 

- Transforming standard list
- Built-in functions
- Generating random data

### Random

Lots of built-in random functions

### Useful Attributes and Method Calls

- np.arrange()
- array.reshape()
- array.max(), .min(), .argmax(), .argmin()
- array.shape
- array.dtype

## Indexing and Selection

- Grabbing single element
- Grabbing a slice of elements
- Broadcasting selections
- Indexing and selection in 2-dim
- Conditional Selection

### Broadcasting and Slicing

With NumPy arrays, we can broadcast a single value across a larger set of values. Slicing section of an array and setting it to a new variable only acts as a pointer to the original array (use the copy method to avoid this).

Examples: [1,2]*2 = [1,2,1,2] versus np.array([1,2]*2) = array([2,4])

[Broadcasting - NumPy v1.19 Manual](https://numpy.org/doc/stable/user/basics.broadcasting.html)

[What is :: (double colon) in numpy like in myarray[0::3]?](https://stackoverflow.com/questions/7123888/what-is-double-colon-in-numpy-like-in-myarray03)

### Operations

[Universal functions (ufunc) - NumPy v1.19 Manual](https://numpy.org/doc/stable/reference/ufuncs.html)

- */0 gives a warning (not an error) and it outputs a result (limit of the operation or nan if the object is not defined)
- consider axis logic when performing operations on arrays

# 🐼 Pandas

Important library for cleaning & organising data and exploratory data analysis. Open source library for data analysis. Uses extremely powerful table object called DataFrame (system) built of NumPy. 

[Tutorials - pandas 0.23.1 documentation](https://pandas.pydata.org/pandas-docs/version/0.23.1/tutorials.html)

[](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

Motivation: 

- Tools for reading and writing data between many formats
- Intelligently grad data based on indexing, logic, subsetting, etc.
- Handle missing data
- Adjust and restructure data

Overview: 

- Series and DataFrames
- Conditional Filtering and Useful Methods
- Missing Data
- Group by Operations (Aggregating data)
- Combining DataFrames (from different data sources)
- Text Methods and Time Methods
- Inputs and Outputs

## Series

Data structure that holds an array of information along with a named index (as opposed to numeric index). Similar to a map or dictionary.

**Formal definition**: one-dimensional ndarray with axis labels. 

Note that internally the data is still numerically organised. A Series has two columns for the user (and three columns internally). First column in the index, second column the data. 

We can combine Series with a shared index to create a tabular data structure called a DataFrame. 

- Since they're built off NumPy arrays we can perform broadcasted operations on them
- If there are problems with the keys while performing broadcasted operations, Pandas returns NaN
- Performing numeric computations with Panda objects, will convert the data into floating numbers. To avoid this we can round with np.round() or pd.round() or specify / hardcode the data type in the operations
- We can name Series when creating them

## DataFrames

Table of columns and rows that can be easily restructured and filtered. We can combine Series that share the same index. Each individual column in the table is a Series and all the Series in the DataFrame share the same index

**Formal definition**: group of Pandas Series objects that share the same index

Basics: 

- Create a DataFrame
- Grab a column or multiple columns
- Grab a row or multiple rows
- Insert a new column or new row

Each column represent a feature / variable and each row represents instance of a data point / entry

Working with Rows

df.loc['index'] similar to Excel's lookup function

### Conditional Formating

Typically in data analysis the datasets are large enough that we don't filter based on position, but instead based on a (column) condition. Conditional filtering allows us to select rows based on condition on a column. This lead to a discussion on organising out data. 

Organising data: **columns are features** (attribute / property of every single instance / row), r**ows are instances of data**. This format is required for ML later on! 

For df['column']>x, Pandas broadcast the comparison to every single instance in the column. Pandas returns a Series of boolean values. We broadcast this series across the entire array: df[df['column']>x] 

Overview: 

- Filter by single condition
- Filter by multiple conditions (operators: & and |)
- Check against multiple possible values (categorical values): is in method

## Useful Methods

[API reference - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/reference/index.html)

Series and DataFrames have specialised methods of calls that are very useful. Check the API reference above if necessary. 

### Apply Method a Single Column

We can use the .apply() method call to apply any custom function to every row in a Series. We can use either one or multiple columns as input. We argument of .apply() is just the function number, we do not call the function! Apply function should return just a single value, as .apply() applies the function for each row in the series (single cell)

### Apply Method on Multiple Columns

Lambda expression are very useful when calling the apply method on multiple columns of the DataFrame. 

Structure: 

- select the columns we're going to be using in the function
- call lambda in the DataFrame
- pass the columns being used to the function
- specify the axis

This structure is expandable to N columns. There is an alternative to make this operation a faster and with a simples syntax: we vectorise the function using NumPy and we call the relevant columns as arguments. 

[How do I select a subset of a DataFrame? - pandas 1.1.5 documentation](https://pandas.pydata.org/docs/getting_started/intro_tutorials/03_subset_data.html)

[Applying function with multiple arguments to create a new pandas column](https://stackoverflow.com/questions/19914937/applying-function-with-multiple-arguments-to-create-a-new-pandas-column)

[Using Numpy Vectorize on Functions that Return Vectors](https://stackoverflow.com/questions/3379301/using-numpy-vectorize-on-functions-that-return-vectors)

### Describing and Sorting

- describe method (transpose the DataFrame to make it more readable)
- sort_values method
- boolean series are usually used as filters

[pandas idxmax: return all rows in case of ties](https://stackoverflow.com/questions/52588298/pandas-idxmax-return-all-rows-in-case-of-ties)

## Missing Data

Options for Missing Data (depending on the situation): 

- Keep it
    - PROS:
        - easiest to do
        - does not manipulate or change the true data
    - CONS:
        - many methods do not support NaN
        - often there are reasonable guesses
- Remove it
    - PROS:
        - easy to do
        - can be cased on rules
    - CONS:
        - potential to lose a lot of data or useful information
        - limits trained model for future data
- Replace it / Filling in the missing data
    - PROS:
        - potential to save a lot of data for use in training a model
    - CONS
        - hardest to do and somewhat arbitrary
        - potential to lead to false conclusions

Dropping a row makes sense when a lot of info is missing > it's good practice to calculate what percentage of data is being dropped 

Dropping a column is a good choice if every row is missing that particular feature

Fill in data if NaN was just a placeholder for another value ,e.g. NaN is a placeholder for a zero. Filling with interpolated or estimated value > much harder and requires reasonable assumptions. We can fill in NaN values with an arbitrary value, the mean, or an (linearly) interpolated value. 

Comparison on NaN-values are done with the 'is' keyword. 

[ROADMAP: Consistent missing value handling with new NA scalar · Issue #28095 · pandas-dev/pandas](https://github.com/pandas-dev/pandas/issues/28095)

[pandas.DataFrame.interpolate - pandas 1.1.5 documentation](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.interpolate.html)

## GroupBy Operations

A groupby() operation allows us to examine data on a **per category** basis > aggregate a continuous value per category. We need to choose a **categorical** column to call with groupby(), i.e. a columns with non-continous values. Note that the values can still be numerical, e.g. Class 1, ..., Class N or Production dates 1970, ..., YYYY. 

We usually (1) call .groupby() (separation) and (2) aggregate the data by grouping / category (evaluation), e.g. sum(), mean(), count(). 

Note that calling .groupby() by itself creates a *lazy* groupby object waiting to be evaluated by an aggregate method call.

Common Options for Aggregate Method Calls:

```
mean(): Compute mean of groups
sum(): Compute sum of group values
size(): Compute group sizes
count(): Compute count of group
std(): Standard deviation of groups
var(): Compute variance of groups
sem(): Standard error of the mean of groups
describe(): Generates descriptive statistics
first(): Compute first of group values
last(): Compute last of group values
nth() : Take nth value, or a subset if n is a list
min(): Compute min of group values
max(): Compute max of group values
```

[GroupBy - pandas 1.1.5 documentation](https://pandas.pydata.org/docs/reference/groupby.html)

Note that we can specify what aggregate function to call on each column. 

Grab based on Cross-Section: it is important to filter out DataFrame first, and then grouping the resulting DataFrame. Concatenation is simply "pasting" the two DataFrames together either based columns or rows (NaN will be filled in automatically)

## Combining DataFrames

[Merge, join, concatenate and compare - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html)

### Concatenate

Data might exist in two separate sources and combining them might be necessary. The simplest combination is if both sources are already in the same format, then a concatenation through the pd.concat() call is all we need. 

### Merge

Merges are often shows as a Venn diagram 

Inner Merge: often DataFrames are not in the exact order or format > we cannot simply concatenate them together > we need to merge the DataFrames (analogous to JOIN command in SQL)

There .merge() method takes in a key argument labeled **how**; there are three main ways of merging tables using the how parameter: 

1. Inner: the result will be the set of records that **match in both** tables
2. Left or Right: all the values on left / right table will be present in the resulting table
3. Outer: all values will be present in the resulting table

The main idea behind the argument is to decide **how** to deal with information only present in one of the joined tables. First, we decide **on** what column to merge together. Important: 

1. the on column should be a primary (unique) identifier (for the row) 
2. the on column should be present in both tables being merge & represent the same thing in both

Second, we decide how to merge the tables on the selected column. 

We can also merge on an index instead of a column 

## Text Methods for String Data

[Working with text data - pandas 1.1.5 documentation](https://pandas.pydata.org/docs/user_guide/text.html)

Often text data needs to be cleaned or manipulated for processing. While we can always use a custom apply() function for these tasks, Pandas comes with many built-in sting method calls.

## Time Methods for Date and Time Data

[Time series / date functionality - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#converting-to-timestamps)

[datetime - Basic date and time types - Python 3.9.1 documentation](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes)

[pandas.DataFrame.resample - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.resample.html)

[pandas.Series.dt - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.html)

Python has a **datetime** (as well as date and time) object containing date and time information. Pandas allows us to extract information from a datetime object (with so called .dt methods) to use feature engineering (in machine learning). 

For example, we may have recent timestamped sales data. We're trying to predict whether or not a customer is going to buy something based off historical trends. Pandas allows us to extract info from the timestamp, e.g. day of the week, weekend vs weekday, AM vs PM. Many ML models do not fully understand datetime objects, but they can understand more categorical data. 

A common operation is resampling or grouping by when the actual time series has the time as the index (time index is a datetime object / timestamp column) . 

## Input and Output

[IO tools (text, CSV, HDF5, ...) - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html)

Pandas can read in data from a wide variety of sources and has excellent online documentation. We may need passwords / permissions for certain data inputs, e.g. SQL database password.

### CSV Files

We need to know the exact directory location and correct file name

### HTML Tables

HTML tables: websites display tabular info through the use of HTML tables tags: <table> </table>. Pandas can automatically convert these HTML tables into a DataFrame. 

Not every table in a website is available through HTML tables. Some websites may block your computer from scraping the HTML of the site through Pandas (> use Beautiful Soup for Web Scraping with Python). It may be more efficient to use an API if available. 

### Excel files

[Working with Excel Files in Python](https://www.python-excel.org/)

Using Pandas with Excel requires additional libraries (openpyxl and xlrd). Pandas can only read and write in raw data, it is not able to read in macros, visualisation, or formulas created inside the spreadsheets. Pandas treats an Excel Workbook as a dictionary, with the key being the sheet name and the value being the DataFrame representing the sheet itself > the result is dictionary of DataFrames. 

### SQL Databases

[](https://docs.sqlalchemy.org/en/13/core/connections.html)

[SQLAlchemy 1.4 Documentation](https://docs.sqlalchemy.org/en/13/dialects/)

Pandas can read and write to various SQL engines through the use of a driver and the **sqlalchemy** python library: 

1. Figure out what SQL Engine you're connecting to, e.g. PostgreSQL, MySQL, MS SQL Server
2. Install the appropriate Python driver library, e.g. PostgreSQL > psycopg2, MySQL > pymysql, MS SQL Server > pyodbc
3. Use the [sqlalchemy](https://docs.sqlalchemy.org/en/13/core/connections.html) library to connect to your SQL database with the driver
4. Use the sqlalchemy driver connection with Pandas read_sql method. Pandas can read in entire tables as a DataFrame or actual parse a SQL query through the connection: SELECT * FROM table; 

## Pivot Tables

[Reshaping and pivot tables - pandas 1.1.5 documentation](https://pandas.pydata.org/docs/user_guide/reshaping.html)

Pivot tables allow you to reorganise data, refactoring cells based on columns and a new index. A Data Frame with repeated values can be pivoted for a reorganisation and clarity. We choose columns to define the new index, columns, and values. Notice how the choices for index and column should have repeated values, i.e. len(column) > len(column.unique()). The values should be more or less unique. This method shows no new information, it is merely reorganised. 

It does not make sense to pivot every DataFrame, all of the datasets used in this course will have no need for a pivot table operation to use with machine learning. 

You should first go through this checklist **before** running a pivot(): 

- What question are you trying to answer?
- What would a DataFrame that answers the question look like? Does it need a pivot()?
- What do you want the resulting pivot to look like?

Usually a groupby() call is a better solution to these questions. 

Pandas also comes with a pivot_table method that allows for an additional aggregation function to be called. This could alternatively be done with a groupby() method as well. 

## Notes from the Exercise

- Important function to determine most common value in a Series `value_counts()` for Categorical values. For Numerical values use `sort_values()`method.
- Use lambda functions and np.vectorize more!
- Break the code into chunks if necessary, for example:

```python
h['kids'] = h['babies'] + h['children']
# add the feature kids = babies + children
positions = h['kids'].nlargest(5).index.values
# kids:S->[0,10]; grad the relevant index positions in the feature (5 largest)
h.iloc[positions][['name','adults','kids','babies','children']]
# locate by index, print relevant columns
```

# 📈 Matplotlib

Visualizing data is crucial to quickly understanding trends and relationships in your dataset matplotlib is knows as the 'grandfather' of plotting and visualization libraries for Python. Many other visualization libraries are built directly off of matplotlib (e.g. seaborn and pandas built-in visualization). 

Matplotlib is heavily inspired by the plotting function of the MatLab programming language. It allow for the creation of almost any plot type and heavy customization. This ability to heavily customize a plot comes at a trade-off for beginners, since it can be confusing to learn the syntax at first. This is mainly due to the fact that there are two separate approaches to creating plots, functional based methods and OOP based methods. 

Specialized plot types, e.g. histograms, won't be covered in this section, since seaborn is a better tool to create statistical plots. 

In Matplotlib Basics we use the functional method; on Matplotlib Figures and Subplots the OOP method. 

Topics: 

- Basics and Functions
- Figures
- Subplots
- Styling

[Matplotlib: Python plotting - Matplotlib 3.3.3 documentation](https://matplotlib.org/)

[Thumbnail gallery - Matplotlib 2.0.2 documentation](https://matplotlib.org/gallery.html)

[](https://matplotlib.org/3.1.1/gallery/index.html)

Goals: 

- Plot out a functional relationship (y=ax) (plotting a known relationship from an equation)
- Plot out a relationship between raw data points (x=[x_1,x_2,x_3,x_4], y=[y_1,y_2,y_3,y_4]) (plotting raw data points)

## Basics

The most basic way to use matplotlib is though the function plot class: `plt.plot(x,y`. These function calls are simple to use, but don't allow for very high degrees of control > quickly visualize relationships and data. Later we will explore the more robust OOP Matplotlib Figure API. 

## Figure Object

The more comprehensive Matplotlib OOP API makes use of a Figure object. We then add axes to this Figure object and then plot on those axes. This allows for very robust controls over the entire plot. 

1. Create the figure object with the `plt.figure()` method and adjust high level parameters, e.g. figure size or dots per inch (and assign it a variable)
2. Add a set of axes to the figure with the `.add_axes()` method and assign it to a variable 
3. Plot on top of that set of axis with the `.plot()` method

Important when saving to use `fig.savefig('figure.png', bbox_inches='tight')` 

## Subplots Functionality

We can create a Figure object and manually add and arrange sets of axes to line up multiple plots side by side. However, matplotlib comes with a pre-configured function call `plt-subplots()`that automatically does this. 

This call allows us to easily create Figure and Axes objects in side by side formations. The call `plt.subplots()` return a tuple which by convention we label `(fig,axes)`: `fig` in the entire Figure canvas and `axes` is a numpy array holding each of the axes according to position in the overall canvas. 

[matplotlib.pyplot.subplots_adjust - Matplotlib 3.2.2 documentation](https://matplotlib.org/3.2.2/api/_as_gen/matplotlib.pyplot.subplots_adjust.html)

## Styling

Matpotlib offers very robust styling functions that allow us to edit colors, legends, line widths, markers, etc. 

Stylings: 

- [Legends](https://matplotlib.org/tutorials/intermediate/legend_guide.html)
- Visual Styling
    - Colors (with [HEX Color Picker](https://www.w3schools.com/colors/colors_picker.asp))
    - Editing Lines
        - Colors, Widths, Styles `possible linestyle options ‘--‘, ‘–’, ‘-.’, ‘:’, ‘steps’`
    - Editing [Markers](https://matplotlib.org/3.2.2/api/markers_api.html)
        - Colors, Size, Styles, Edges

## Advanced Commands

Almost any Matplotlib question you can think of already has an answer in StackOverflow or an example in the Matplotlib gallery > leaverage these many examples to your advantage and do not waste energy and time into memorizing esoteric commands! 

# 🌊 Seaborn

Start here! 

# 🔧 Open Questions and Tasks

## Open Questions

- What are our categorical columns to group by?
- Do we need to use datetime objects in our project?

## Backlog

- Crapstone
- Linear Regression
- Logistics Regression
- Machine Learning
- Revise the lecture before the presentation!

## In Progress

- Seaborn
- Apply Panda lessons to project
- Convert [rawTimesamp](https://stackoverflow.com/questions/19231871/convert-unix-time-to-readable-date-in-pandas-dataframe) feature into a datetime object > useful later for feature engineering (see [documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html))
- Make an outline of the project
- Decide what are the relevant categorial columns for the project
- Make a [data column reference](https://www.notion.so/ac02bfefe61246918aabf0e6094f18c9) in HTML (see [data type](https://en.wikipedia.org/wiki/Data_type), [7 data types](https://towardsdatascience.com/7-data-types-a-better-way-to-think-about-data-types-for-machine-learning-939fae99a689); use Notion or [Tables Generator](https://www.tablesgenerator.com/html_tables))
- Strip project data
- Make sure there is no missing data in the project

## Resolved

- Matplotlib
- Pandas
- Numpy
- Machine Learning Pathway
- Python Crash Course
- Upload files to Github
- Do crash course on Git

## Workflow

- pull repo
- work on project
- update README
- push repo

# 📋 Outline of Project (WIP)

- Create DataFrames
- Apply Pandas knowledge to DataFrame
    - Conditional filtering
    - Useful Methods
    - Check for missing data

# 💡 Misc

$PATH is stored in /etc/paths; open with sudo nano to modify 

Can we model the process in the project as a Poisson process?

`pd.options.display.float_format = "{:,.2f}".format` > `pd.set_option('float_format', '{:f}'.format)`  

[Python - Check If Word Is In A String](https://stackoverflow.com/questions/5319922/python-check-if-word-is-in-a-string)

[Why does Python code use len() function instead of a length method?](https://stackoverflow.com/questions/237128/why-does-python-code-use-len-function-instead-of-a-length-method)

[Code Faster with Line-of-Code Completions, Cloudless Processing](https://www.kite.com/python/answers/how-to-display-float-values-in-a-pandas-dataframe-to-two-decimal-places-in-python)

[string - Common string operations - Python 3.9.1 documentation](https://docs.python.org/3/library/string.html#format-specification-mini-language)

[Python String format() Method](https://www.w3schools.com/python/ref_string_format.asp)

[Dashboarding with Jupyter Notebooks, Voila and Widgets | SciPy 2019 | M. Breddels and M. Renou](https://www.youtube.com/watch?v=VtchVpoSdoQ)

[Building Interactive Applications and Dashboards in the Jupyter Notebook](https://www.youtube.com/watch?v=i40d8-Hu4vM)

[How do I print entire number in Python from describe() function?](https://stackoverflow.com/questions/41328633/how-do-i-print-entire-number-in-python-from-describe-function)

[15. Floating Point Arithmetic: Issues and Limitations - Python 3.9.1 documentation](https://docs.python.org/3/tutorial/floatingpoint.html)

[% (String Formatting Operator) - Python Reference (The Right Way) 0.1 documentation](https://python-reference.readthedocs.io/en/latest/docs/str/formatting.html)

[How to save Jupyter's environment (and kernels)](https://kiwidamien.github.io/save-jupyters-environment)

[Visualize any Data Easily, from Notebooks to Dashboards | Scipy 2019 Tutorial | James Bednar](https://www.youtube.com/watch?v=7deGS4IPAQ0)