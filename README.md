# Statistics Meets Logistics

The [course](https://www.statistik.tu-dortmund.de/2791.html) and the [material](https://moodle.tu-dortmund.de/enrol/index.php?id=22199) provided by the lecturer are in German. The documentation is in English. This repository documents our progress in preparation for the project and holds the project and its data. 

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

## Jupyter Notebook

Version control with Git: 

[Reproducible Data Analysis in Jupyter, Part 3/10: Version Control with Git & GitHub](https://www.youtube.com/watch?v=J45NJ0pJXWQ)

Useful shortcuts in Jupyter notebook: 

[Jupyter Tips and Tricks](https://www.youtube.com/watch?v=2eCHD6f_phE&t=0s)

[My favorite Jupyter notebook shortcuts](https://www.youtube.com/watch?v=FW2BF6jbHBk)

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

This is the section for the Python crash course. [Current Python documentation](https://docs.python.org/3/contents.html).

## Crash Course

If a variable is being highlighted by the IDE, this keyword is reserved for an object!

- String interpolation / [.format()](https://pyformat.info/) on string = a way to insert things into a string
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

Important library for cleaning & organising data and exploratory data analysis. Open source library for data analysis. Uses extremely powerful table object called DataFrame (system) built off NumPy. 

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

[Applying function with multiple arguments to create a new pandas column](https://stackoverflow.com/questions/19914937/applying-function-with-multiple-arguments-to-create-a-new-pandas-column)

[Using Numpy Vectorize on Functions that Return Vectors](https://stackoverflow.com/questions/3379301/using-numpy-vectorize-on-functions-that-return-vectors)

### Describing and Sorting

- describe method (transpose the DataFrame to make it more readable)
- sort_values method
- boolean series are usually used as filters

[pandas idxmax: return all rows in case of ties](https://stackoverflow.com/questions/52588298/pandas-idxmax-return-all-rows-in-case-of-ties)

# 🔧 Open Questions and Tasks

## Open Questions

- Was ist CQI?
- Was is TA?
- Was ist CI?
- Was ist ID?
- Ist die Variable 'distance' relevant für unsere Analyse?

## Backlog

- Watch [collaboration in Git and Jupyter notebook](https://www.youtube.com/watch?v=J3k3HkVnd2c) for ideas
- Matplotlib
- Seaborn
- Crapstone
- Linear Regression
- Logistics Regression
- Machine Learning

## In Progress

- Pandas

## Resolved

- Do crash course on Git
- Upload files to Github
- Python Crash Course
- Machine Learning Pathway
- Numpy

## Workflow

- pull repo
- work on project
- update README
- push repo

# 💡 Misc

- $PATH is stored in /etc/paths; open with sudo nano to modify
- [Check if word in in a string](https://stackoverflow.com/questions/5319922/python-check-if-word-is-in-a-string)
- [https://stackoverflow.com/questions/237128/why-does-python-code-use-len-function-instead-of-a-length-method](https://stackoverflow.com/questions/237128/why-does-python-code-use-len-function-instead-of-a-length-method)
- Can we model the process in the project as a Poisson process?