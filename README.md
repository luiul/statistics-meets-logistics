# Statistics Meets Logistics

The [course](https://www.statistik.tu-dortmund.de/2791.html) and the [material](https://moodle.tu-dortmund.de/enrol/index.php?id=22199) provided by the lecturer are in German. This repository documents our preparation for the project and holds the project and its data. 

To view LaTeX equations found in *Introduction to Linear Regression* and subsequent Sections, consider the following options: 

- Open the [.HTML version of the README](https://htmlpreview.github.io/?https://github.com/luiul/statistics-meets-logistics/blob/main/README.html)
- Preview directly on Github using a browser [extension](https://github.com/AaronCQL/katex-github-chrome-extension) (Chromium based)
- Copy the equation block directly from the [raw README](https://raw.githubusercontent.com/luiul/statistics-meets-logistics/main/README.md) and use a LaTeX [renderer](https://quicklatex.com/) or [image generator](https://github.com/masakiaota/tex_image_link_generator)

# 📖 Description

In the course, students will learn about the application of statistical methods and basic machine learning procedures for the analysis of complex data in the field of logistics. This includes methods of descriptive statistics as well as various regression and classification procedures including neural networks. After the introduction of the methods, the students apply the acquired knowledge independently to work on logistical problems in various practical exercises. The software Python and relevant packages are used.

# 📑 Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<!-- END doctoc -->

- [🌅 Background](#-background)
  - [Getting Started with Anaconda](#getting-started-with-anaconda)
  - [Jupyter Notebook](#jupyter-notebook)
  - [JupyterLab](#jupyterlab)
  - [VS Code](#vs-code)
  - [Version Control with Git](#version-control-with-git)
  - [Basic Markdown](#basic-markdown)
  - [Virtual Environments](#virtual-environments)
  - [Activate the virtual environment](#activate-the-virtual-environment)
- [🐍 Python Crash Course](#-python-crash-course)
  - [Crash Course](#crash-course)
- [🤖 Machine Learning Pathway](#-machine-learning-pathway)
  - [Meta-Pathway](#meta-pathway)
  - [Pathway](#pathway)
- [🥧 NumPy](#-numpy)
  - [Array](#array)
    - [Random](#random)
    - [Useful Attributes and Method Calls](#useful-attributes-and-method-calls)
  - [Indexing and Selection](#indexing-and-selection)
    - [Broadcasting and Slicing](#broadcasting-and-slicing)
    - [Operations](#operations)
- [🐼 Pandas](#-pandas)
  - [Series](#series)
  - [DataFrames](#dataframes)
    - [Conditional Formating](#conditional-formating)
  - [Useful Methods](#useful-methods)
    - [Apply Method a Single Column](#apply-method-a-single-column)
    - [Apply Method on Multiple Columns](#apply-method-on-multiple-columns)
    - [Describing and Sorting](#describing-and-sorting)
  - [Missing Data](#missing-data)
  - [GroupBy Operations](#groupby-operations)
  - [Combining DataFrames](#combining-dataframes)
    - [Concatenate](#concatenate)
    - [Merge](#merge)
  - [Text Methods for String Data](#text-methods-for-string-data)
  - [Time Methods for Date and Time Data](#time-methods-for-date-and-time-data)
  - [Input and Output](#input-and-output)
    - [CSV Files](#csv-files)
    - [HTML Tables](#html-tables)
    - [Excel files](#excel-files)
    - [SQL Databases](#sql-databases)
  - [Pivot Tables](#pivot-tables)
  - [Notes from the Exercise](#notes-from-the-exercise)
- [📊 Matplotlib](#-matplotlib)
  - [Basics](#basics)
  - [Figure Object](#figure-object)
  - [Subplots Functionality](#subplots-functionality)
  - [Styling](#styling)
  - [Advanced Commands](#advanced-commands)
- [🌊 Seaborn](#-seaborn)
  - [Scatter Plots](#scatter-plots)
  - [Distribution Plots](#distribution-plots)
  - [Categorical Plots - Statistics within Categories](#categorical-plots---statistics-within-categories)
  - [Distributions within Categories](#distributions-within-categories)
  - [Comparison Plots (!)](#comparison-plots-)
  - [Grids](#grids)
  - [Matrix Plots](#matrix-plots)
  - [Notes from Exercise](#notes-from-exercise)
- [🗿 Capstone Project](#-capstone-project)
  - [Normalization](#normalization)
- [🏔 Machine Learning Concepts Overview](#%F0%9F%8F%94-machine-learning-concepts-overview)
  - [Why Machine Learning?](#why-machine-learning)
  - [Types of ML Algorithms](#types-of-ml-algorithms)
    - [Supervised Learning](#supervised-learning)
    - [Unsupervised Learning](#unsupervised-learning)
  - [Supervised ML Process](#supervised-ml-process)
- [📏 Introduction to Linear Regression](#-introduction-to-linear-regression)
  - [Algorithm History](#algorithm-history)
  - [OLS Equations](#ols-equations)
  - [Cost Functions](#cost-functions)
  - [Gradient Descent](#gradient-descent)
  - [Coding Simple Linear Regression with Python](#coding-simple-linear-regression-with-python)
- [📚 Scikit-learn](#-scikit-learn)
  - [Linear Regression with Scikit-learn](#linear-regression-with-scikit-learn)
    - [Data Setup and Model Training](#data-setup-and-model-training)
  - [Performance Evaluation with Scikit-learn - Regression Metrics](#performance-evaluation-with-scikit-learn---regression-metrics)
    - [Mean Absolute Error (MAE)](#mean-absolute-error-mae)
    - [**Mean Squared Error** (MSE)](#mean-squared-error-mse)
    - [**Root Mean Squared Error** (RMSE)](#root-mean-squared-error-rmse)
  - [Evaluating Residuals](#evaluating-residuals)
  - [Model Deployment and Coefficient](#model-deployment-and-coefficient)
- [🦑 Polynomial Regression](#-polynomial-regression)
  - [Bias Variance Trade-Off: Overfitting versus Underfitting (based on MSE)](#bias-variance-trade-off-overfitting-versus-underfitting-based-on-mse)
- [🍡 Regularization and Cross Validation](#-regularization-and-cross-validation)
  - [Feature Scaling and Regularization](#feature-scaling-and-regularization)
  - [Cross Validation](#cross-validation)
    - [Principle](#principle)
    - [Hold Out Test Set](#hold-out-test-set)
    - [Regularization Data Setup](#regularization-data-setup)
  - [L2 Regularization - Ridge Regression](#l2-regularization---ridge-regression)
- [🔧 Open Questions and Tasks](#-open-questions-and-tasks)
  - [Open Questions](#open-questions)
  - [Backlog](#backlog)
  - [In Progress](#in-progress)
  - [Resolved (Preparation)](#resolved-preparation)
  - [Resolved (Project)](#resolved-project)
  - [Workflow](#workflow)
- [📋 Outline of Project (WIP)](#-outline-of-project-wip)
- [💡 Misc](#-misc)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

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

See [themes](https://stackoverflow.com/questions/46510192/change-the-theme-in-jupyter-notebook). See [extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions), e.g. [variable explorer](https://stackoverflow.com/questions/37718907/variable-explorer-in-jupyter-notebook). Version control with Git: 

[Reproducible Data Analysis in Jupyter, Part 3/10: Version Control with Git & GitHub](https://www.youtube.com/watch?v=J45NJ0pJXWQ)

Useful shortcuts in Jupyter notebook: 

[Jupyter Tips and Tricks](https://www.youtube.com/watch?v=2eCHD6f_phE&t=0s)

[My favorite Jupyter notebook shortcuts](https://www.youtube.com/watch?v=FW2BF6jbHBk)

## JupyterLab

[JupyterLab](https://github.com/jupyterlab/jupyterlab) is the next-gen user interface for Project Jupyter offering all the familiar building blocks of the classic Jupyter Notebook (notebook, terminal, text editor, file browser, rich outputs, etc.) in a flexible and powerful user interface. JupyterLab will eventually replace the classic Jupyter Notebook. [Kite](https://github.com/kiteco/jupyterlab-kite) is available for Jupyterlab. 

[Contributing to JupyterLab - JupyterLab 2.3.0a2 documentation](https://jupyterlab.readthedocs.io/en/stable/developer/contributing.html?highlight=virtual%20environment#installing-jupyterlab)

[How to add conda environment to jupyter lab](https://stackoverflow.com/questions/53004311/how-to-add-conda-environment-to-jupyter-lab)

[mauhai/awesome-jupyterlab](https://github.com/mauhai/awesome-jupyterlab)

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

1. Import `requirements.txt` as Conda explicit specification file in the Anaconda Navigator
2. Run the following command in the command prompt interface (Anaconda prompt or directly in the terminal):

`conda create --name <envName> jupyter==1.0.0 lxml==4.5.1 MarkupSafe==1.1.1 matplotlib==3.3.2 notebook==6.0.3 numpy==1.18.1 openpyxl==3.0.4 pandas==1.1.2 Pillow==7.2.0 scikit-learn==0.23.2 scipy==1.4.1 seaborn==0.11.0 SQLAlchemy==1.3.18 xlrd==1.2.0`

or

`conda create --prefix ~/opt/anaconda3 jupyter==1.0.0 lxml==4.5.1 MarkupSafe==1.1.1 matplotlib==3.3.2 notebook==6.0.3 numpy==1.18.1 openpyxl==3.0.4 pandas==1.1.2 Pillow==7.2.0 scikit-learn==0.23.2 scipy==1.4.1 seaborn==0.11.0 SQLAlchemy==1.3.18 xlrd==1.2.0`

## Activate the virtual environment

There are two options: 

1. On the Anaconda Navigator: Environments tab > choose the environment > open application on the environment
2. In the terminal: `conda active <myEnv>` (replace `<myEnv>` the name of your environment)

# 🐍 Python Crash Course

This is the section for the Python crash course. [Python documentation](https://docs.python.org/3/contents.html). [Python Built-in Functions](https://docs.python.org/3/library/functions.html). 

## Crash Course

Keep the following points in mind when working with Python: 

- If a variable is being highlighted by the IDE, this keyword is reserved for an object!
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

[Index of element in NumPy array](https://stackoverflow.com/questions/18079029/index-of-element-in-numpy-array)

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

[Indexing and selecting data - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy)

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

[Merge two dataframes by index](https://stackoverflow.com/questions/40468069/merge-two-dataframes-by-index)

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

Usually a groupby() call is a better solution  1wto these questions. 

Pandas also comes with a pivot_table method that allows for an additional aggregation function to be called. This could alternatively be done with a groupby() method as well. 

## Notes from the Exercise

- See [styling documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/style.html) for more styling options.
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

# 📊 Matplotlib

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

- [Legends](https://matplotlib.org/tutorials/intermediate/legend_guide.html) (see also [stack overflow question](https://stackoverflow.com/questions/39803385/what-does-a-4-element-tuple-argument-for-bbox-to-anchor-mean-in-matplotlib/39806180#39806180))
- Visual Styling
    - Colors (with [HEX Color Picker](https://www.w3schools.com/colors/colors_picker.asp))
    - Editing Lines
        - Colors, Widths, Styles
    - Editing [Markers](https://matplotlib.org/3.2.2/api/markers_api.html)
        - Colors, Size, Styles, Edges

## Advanced Commands

Almost any Matplotlib question you can think of already has an answer in StackOverflow or an example in the Matplotlib gallery > leaverage these many examples to your advantage and do not waste energy and time into memorizing esoteric commands! 

# 🌊 Seaborn

[seaborn: statistical data visualization - seaborn 0.11.0 documentation](https://seaborn.pydata.org/)

Statistical plotting library designed to interact well with Pandas DataFrames to create common statistical plot types. It is built directly off of Matplotlib but uses a simpler syntax > we trade-off customization for ease of use. However, since its built directly off of Matplotlib, we can still make plt method calls to directly affect the resulting seaborn plot > seaborn is an abstraction above Matplotlib commands (with the same figure object and axes objects). 

A typical seaborn plot uses one line of come, e.g.

```python
sns.scatterplot(x='salary', y='sales', data=df)
```

Seaborn takes in the DataFrame and then the user provides the corresponding string column names for x and y (depending on the plot type). It is important to focus on understanding the use cases for each plot and the seaborn syntax for them. 

It is important to understand the question you're trying to answer. If a visualization is useful you can google 'choosing a plot visualization' for useful flowcharts on the topic.

Overview: 

- Scatter Plots
- Distribution Plots
- Categorical Plots
- Comparison Plots
- Seaborn Grids
- Matrix Plots

## Scatter Plots

**continuous feature + categorical hue**

 **x = cont_feature1, y = cont_feature2**

---

Scatter plots show the relationship between two continuous features. Recall that **continuous** feature are numeric variables that can take any number of values between any two values, e.g. age, height, salary, temperature, prices, etc.

A continuous feature allow for a value to always be between two values. This is not b confused with **categorical** features which represent distinct and unique categories, e.g. colors, shapes, names, etc. 

Scatter plots line up a set of two continuous features and plots them out as coordinates. Example: employees with salaries who sell a certain dollar amount of items each year. We could explore the relationship between employee salaries and sales amount. 

You can choose a [color palette](https://matplotlib.org/tutorials/colors/colormaps.html) for the plot with the parameter `palette`. 

**The `hue` parameter determines which columns in the data frame should be used for color encoding (parameter is a categorical feature; commonly use in seaborn plots).** 

## Distribution Plots

**continuous feature**

**x = cont_feature, y = count**

---

In this section we use a [data generator](http://roycekimmons.com/tools/generated_data). 

Distribution plots display a single continuous feature and help visualize properties such as deviation and average values. There are 3 main distribution plot types: 

- Rug Plot: simplest distribution plot; it merely adds a dash or tick line for every single value (one dimensional scatter plot with one variable)
    - CONS:
        - the y-axis contains no information / not interpretable
        - many ticks can be on top of each other but we can't tell
    - PROS:
        - it's easy to see outliers
- Histogram: essentially a modified rug plot. If we count how many ticks there are per various x-ranges, we can create a histogram.
    1. we choose the number of "bins", i.e. the number and size of intervals
    2. we count the number of data points / instances in the intervals
    3. we create a bar as high as count

    Note that we can normalize the Y-axis as a percentage. Changing the number and size of the intervals show more detail instad of general trends. 

- KDE Plot (Kernel Density Estimation): Seaborn allows us to add on a KDE plot curve on top of a histogram. It shows what a continuous PDF would look like for this particular dataset. KDE is a method of **estimating** PDF of a random variable > it's a way of estimating a continuous probability curve for a finite data sample. Construction:
    1. we start off with a rug plot 
    2. we decide what kernel to use, i.e. what probability distribution do we want to stack on top of each instance
    3. we sum all distributions to come up the KDE plot
    4. if the values are outside the image of the random variable we can make a hard cut on the plot (and renormalize)

    Note that we can change the kernel and the bandwidth used on the KDE to show more or less of the variance contained in the data

continue here

## Categorical Plots - Statistics within Categories

**categorical feature**

 **x = cat_feature, y = estimator**

---

The categorical plots discussed here will display a statistical metric **per** category, e.g. mean value per category or a count of the number of row per category > it is the visualization equivalent of a `groupby()` call. 

The two main types of plots for this are: 

- `countplot()` to count number of rows per category. We can display more information in the plot with the addition of hue separation.
- `barplot()` which is the general form of displaying any chosen metric (measure or estimator) per category, e.g. the mean value or standard deviation. Note: be careful when using these plots, since the bar is filled and continuous, a viewer may interpret continuity along the y-axis which may be incorrect! > Always make sure to add additional labeling and explanation for these plots! > since this are single values it is probably better to report this in a table

## Distributions within Categories

**grouped continuous feature**

 **x = cat_feature, y = cont_feature**

---

We explored distributions plots for a single feature, i.e. rug plot, histogram and KDE, but what if we want to compare distributions across categories? For example, instead of the distribution of everyone's salary, we can compare the distribution of salaries **per** level of education. We will first separate out each category, then create the distribution visualization. 

Plot types: 

- Boxplot: displays the distribution of a continuous variable. It does this through the use of quartiles. Quartiles separate out the data into 4 equal number of data points: 25% of data points are in bottom quartile. 50th percentile (Q2) is the median. The median splits the data in half (half the data points are to the right / left of it). 
The IQR defines the box width > 50% of all data points are inside the box. 
The whiskers are defined by 1.5 IQR. 
Outside of the whiskers are outliers. 
Boxplots quickly give statistical distribution information in a visual format > we can make a boxplot **per** category. 
Note: the boxplot contains information about the distribution of the data, but not the amount of data points (in a category)
- Violinplot: similar role as the boxplot. It displays the PDF across the data using a KDE. We can imagine it as a mirrored KDE plot.
- Swarmplot: simply shows all the data points in the distribution > this **will** display the number of data points per category
- [Boxenplot](https://vita.had.co.nz/papers/letter-value-plot.html) / Letter-Value Plot: expansion upon the normal box plot. Using a system of letter-values we can use multiple quantiles instead of strictly quartiles.

## Comparison Plots (!)

**continuous feature + categorical hue**

**x = cont_feature1, y = cont_feature2**

---

Comparison plots are essentially 2-dimensional versions of the plots we've learned about so far. The two main plot types discussed here are: 

- jointplot(): map histograms to each feature of a scatterplot to clarify the distribution within each feature. We can also adjust the scatterplot to be a hexagons plot or a 2D KDE plot. 
In the hexagon plot, hexagons are dark the more points fall into their area.
2D KDE plots show shaded distribution between both KDEs.
- pairplot(): quick way to compare all numerical columns in a DataFrame. It automatically creates a histogram for each column and a scatterplot comparison between all possible combinations of columns. pairplot() can be CPU and RAM intensive for large DataFrames with many columns > it is a good idea to first filter down to only the columns you are interested in. We can add a hue parameter. We can do this with an KDE too.

For comparison plots we need two continuous features. 

## Grids

**continuous feature + categorical axis (cols or rows) + categorical hue**

**x = cat_feature, y = cont_feature**

---

Seaborn grid calls use Matplotlib subplots() to automatically create a grid based off a categorical column. Instead of passing in a specific number of cols or row for the subplots, we can simply pass int he name of the column and seaborn will automatically map the subplots grid. 

Many built-in plot calls are running on top of this grid system. Directly calling the grid system allows users to heavily customize plots. Calls: 

- catplot(): takes in cols / rows of categorical features and plots the data by category. It runs on a FacetGrid.
- PairGrid(): pairpot() calls the PairGrid functionality which creates a grid and fills it in. Calling PairGrid makes the grid and wait for mapping commands. We can add a hue in the higher level PairGrid call (note that it doesn't automatically add the legend).

## Matrix Plots

**continuous feature grouped by index**

**x = all_cont_features, y = all_cont_features**

---

Matrix are the visual equivalent of displaying a pivot table. The matrix plot displays all the data passed in, visualizing all the numeric values in a data frame. Note that not every data frame is a valid choice for a matrix plot such as a heatmap. 

The two main matrix plot types are: 

- heatmap(): visually displays the distribution of cell values with a color mapping. Note that a heatmap should ideally have all cells be in the same unit, so the color mapping makes sense across the **entire** data frame. In the example, all values are **rates** of percentage growth or change were in the heatmap. Use cmap instead of palette as a parameter.
- clustermap(): same visual as heatmap, but first conducts **hierarchical clustering** to reorganize data into groups.

Note that seaborn comes with the ability to automatically cluster similar groupings. Later on we will discuss how this clustering is done when we learn about Machine Learning clustering techniques. 

**We often do a heat map on the correlation of the features within machine learning to see what features are good candidates for trying to predict a label!** 

## Notes from Exercise

Main goal of seaborn is to be able to use its simpler syntax to quickly create informative plots. In general its dificult to test on seaborn skills since most plots are simply passing in the data and choosing x and y. Most plots have filtering and adjustments with pandas on the data frame **before** being passed into the seaborn call. 

# 🗿 Capstone Project

We put our current skills together with a Capstone Project. 

Review: we start from the real world and we start two main approaches: 

1. Problem to Solve: How to fix or change X? 
2. Question to Answer: How does a change in X affect Y? 

We have the basic skill set to perform basic data analysis (Jupyter Notebook + NumPy + Pandas + Matplotlib + Seaborn): 

1. Real World
2. Collect & Store Data 
3. Clean & Organize Data
4. Exploratory Data Analysis
    1. Report
    2. Visualization
    3. Communication
5. Data Analysis
6. Real World

Question to answer in this section: is there a conflict of interest for a website that both sells movie tickets **and** displays review ratings? More specifically: does a website like Fandango artificially display higher review rating to sell more movie tickets? 

First compare the start (what user see) and rating (internal) features to check for discrepancies. Then, compare Fandango's rating to other rating website scores. 

[Normalize columns of pandas data frame](https://stackoverflow.com/questions/26414913/normalize-columns-of-pandas-data-frame)

[https://www.codecademy.com/articles/normalization#:~:text=Min-max normalization is one,decimal between 0 and 1.&text=That data is just as squished as before](https://www.codecademy.com/articles/normalization#:~:text=Min%2Dmax%20normalization%20is%20one,decimal%20between%200%20and%201.&text=That%20data%20is%20just%20as%20squished%20as%20before)!

[Not clear how to reposition seaborn.histplot legend · Issue #2280 · mwaskom/seaborn](https://github.com/mwaskom/seaborn/issues/2280)

## Normalization

[Article](https://www.codecademy.com/articles/normalization#:~:text=Min%2Dmax%20normalization%20is%20one,decimal%20between%200%20and%201.&text=That%20data%20is%20just%20as%20squished%20as%20before)

Problem: features are on (drastically) different scales. 

Solution:

- Min-Max Normalization: downside: it does not handle outliers very well.
- Z-Score Normalization: The only potential downside is that the features aren’t on the exact same scale

# 🏔 Machine Learning Concepts Overview

Starting Point: 

We put our current skills together with a Capstone Project. 

Review: we start from the real world and we start two main approaches: 

1. Problem to Solve: How to fix or change X? 
2. Question to Answer: How does a change in X affect Y? 

We have the basic skill set to perform basic data analysis (Jupyter Notebook + NumPy + Pandas + Matplotlib + Seaborn): 

1. Real World
2. Collect & Store Data 
3. Clean & Organize Data
4. Exploratory Data Analysis
    1. Report
    2. Visualization
    3. Communication
5. Data Analysis
6. Real World

We can build:

1. Data Products
2. Data Analysis

After some Exploratory Data Analysis we move onto *Machine Learning Models*; there are two types: 

1. Supervised Learning: Predict an Outcome
2. Unsupervised Learning: Discover Pattern in Data

Goals: 

- Problems solved by ML
- Types of ML
    - Supervised Learning
    - Unsupervised Learning
- ML Process for Supervised Learning
- Discussion on Companion Book

Other important topics: 

- Bias-Variance Trade-off
- Over- versus Underfitting
- Cross-validation
- Feature Engineering
- Scikit-learn
- Performance Metrics

ML Sections: 

- Section for Type of Algorithms
    - Intuition and Mathematical Theory
    - Example code-along of application of Algorithm
    - Expansion of Algorithm
    - Project Exercise
    - Project Exercise Solution

The only exception to this workflow in the Linear Regression section:

- Intuition and Mathematica Theory
- Simple Linear Regression
- Scikit-learn and Linear Regression
- Regularization

The goal of this section is to discover additional ML topics: 

- Performance Metrics
- Feature Engineering
- Cross-Validation

Afterwards, we revisit Linear Regression to combine discovered ML ideas for a final Project Exercise

## Why Machine Learning?

ML is the study of statistical computer algorithms that improve automatically through data > unlike typical computer algorithms that rely on human input for what approach to take, ML algorithms infer best approach from the data itself.

ML is a subset of AI. ML algorithms are not explicitly programmed on which decisions to make. Instead the algorithm is designed to infer from the data the most optimal choices to make. 

What kinds of problems can ML solve? 

- Credit Scoring
- Insurance Risk
- Price Forecasting
- Spam Filtering
- Customer Segmentation

Structure of ML Problem Framing: 

- Given **Features** from a data set **obtain** a desired **Label**
- ML algorithms are often called *estimators* since they are estimating the desired **Label** or output

ML algorithms rely on data and a set of statistical methods to learn what features are important in data. 

Simple Example: predict the price a house should sell at given its current features (area, bedrooms, bathrooms, etc.). f(data) = label, where the label is the sell price. 

House Price Prediction: 

- Typical Algorithm: human user defines an algorithm to manually set values of importance (weights) for each feature
- ML algorithm: Algorithm automatically determines importance (weight) of each feature from existing data > no human has to manually assign the importance of each feature in the data set in order to predict the label. The ML algorithm is going to use statistical methods to determine the importance of each feature to predict the label.

Motivation: 

- Many complex problems are only solvable with ML techniques
- Problems such as spam email or handwriting identifiers require ML for an effective solution

Problems: 

- Major caveat to effective ML is good data
- Majority of development time is spent cleaning and organizing data, **not** implementing ML algorithms

Do we develop our own algorithms? 

- Rarely do we need to manually develop and implement a new ML algorithm, since these techniques are well documented and developed
- We leverage the work that has already been done and can be found in Python libraries

## Types of ML Algorithms

Two main types: supervised and unsupervised learning. 

### Supervised Learning

Supervised Learning: using **historical** and **labeled** data, the machine learning model predicts a value

Requirement: **historical labeled** data: 

- Labeled: the desired output is know (e.g. we know the label, i.e. the price, for the house > in the future we'll be able to predict the label / price of the house based on its features)
- Historical: known results and data from the past (e.g. data from houses sold in the past)

Two main label types: 

- Categorical Value to Predict: Classification Task
- Continuos Value to Predict: Regression Task

Classification Task: 

- Predict an assigned category, e.g. cancerous vs benign tumor (binary), fulfillment vs credit default (binary), assigning image category > handwriting recognition

Regression Task: 

- Predict continuous value: future prices, electricity loads, test scores

### Unsupervised Learning

Unsupervised Learning: applied to **unlabeled** data, the machine learning model discovers possible patterns in the data. 

Groups and interpret data without a label, e.g. clustering customer into separate groups based off their behavior features.

Major downside: there is no historical "correct" label > it is much harder to evaluate performance of an unsupervised learning algorithm 

Here we first focus on supervised learning to build an understanding of ML capabilities. Afterwards, we shift focus to unsupervised leaning for clustering and dimensionality reduction. 

## Supervised ML Process

For (1) collect & store data, (2) clean & organize data, and (3) exploratory data analysis we have jupyter, numpy, pandas, matplotlib, and seaborn. For ML Models, i.e. supervised (outcome prediction) and unsupervised learning (pattern recognition in data), we have **Scikit-learn**.  

Start with collecting and organizing a data set based on history. 

Starting situation: we have **historical labeled** data on previously sold houses. 

Task: create a data product that: if a new house comes on the market with a know Area, Bedrooms, and Bathrooms; predict what price should it sell at. 

Data Product: 

- Input: house features
- Output: predicted selling price

We're using historical, labeled data to predict a future outcome or result. 

The **process**: 

Data > **X: Features, Y: Label** > Training Data Set & Test Data Set > Fit / Train Model > Evaluate Performance > if not satisfied: adjust model > fit / train adjusted model > Evaluate Performance > Deploy Model (as Service, Dashboard or Application > Data Product)

- we have data about the features and labels
- separate the data into features and label
    - X: features (know characteristics or components in the data)
    - Y: label (what are we trying to predict)
- **Features** and **Label** are identified according to the problem being solved
- Split data into training data set and test data set (see cross-validation and hold-out sets)
- We train the ML algorithm on the training data set
- We feed the ML algorithm the features of the test data set & ask predictions per data point
- We compare the prediction y_hat against the true price y & evaluate the performance (we'll discuss the evaluation methods later)
- If we're not satisfied with the performance of the ML algorithm we can adjust the model **hyper-parameter** (many algorithm have adjustable values)

Train / Test Split: 

- We want to be able to fairly evaluate the performance of the ML algorithm.
- Usually, the percentage of training data is larger the percentage of test data.
- We have 4 components of data: X train, Y train, X test and Y test.

# 📏 Introduction to Linear Regression

This section covers: 

- Theory of Linear Regression
- Simple Implementation with Python (and NumPy)
- Scikit-Learn Overview
- Linear Regression with Scikit-learn
- Polynomial Regression (builds on top of Linear Regression)
- Regularization (builds on top of Linear Regression)
- Overview of Project Dataset

Note that the Project Exercise will be spread over many section, since we first discuss **Feature Engineering** and **Cross-Validation** before tackling the full Project Exercise. Note that LaTeX equations are exported directly to the readme file and might not be displayed properly in GitHub. 

[Regression analysis](https://en.wikipedia.org/wiki/Regression_analysis)

## Algorithm History

Before we code, we'll build an intuition of the theory and motivation behind Linear Regression: 

- Brief History
- Linear Relationships
- Ordinary Least Squares
- Cost Functions (and Minimization)
- Gradient Descent
- Vectorization

Relevant Reading in ISLR: 

- Section 3: Linear Regression
    - 3.1 Simply Linear Regression

Basic goal: minimize the residual error (squared) (see 24 Classical Inference, p. 109)

**Ordinary Least Squares** works by minimizing the sum of the squares of the residual error (difference between the observed dependent variable (values of the variable being observed) in the given dataset and those predicted by the linear function).  We can visualize squared errors to minimize (minimize the sum of the areas). 

Having a squared error simplifies out calculation later on when setting up a derivative. We explore OLS by converting a real data set into mathematical notation, then working to solve a linear relationship between features and a variable. 

## OLS Equations

Linear Regression allows us to build a relationship between multiple **features** to estimate a **target output** The linear function `y=mx+b` only has room for a possible feature `x`. OLS allows us to solve for the slope `m` and the intercept `b`. Later, we'll need tools like gradient descent to scale this to multiple features. We can translate this data into generalized mathematical notation: X is the matrix that contains multiple features and y is the vector that contains the label we're trying to predict. We build the linear relationship between the features X and label Y. Note that we're looking for a linear combination to computer an estimate. Also note that in the linear combination we don't have an intercept `b`. 

We consider the 1st degree polynomial for our estimator (see REnADME preamble if LaTeX equation is not rendering): 

$$\hat{y}=b_{0}+b_{1} x$$

$$b_{1}=\rho_{x, y} \frac{\sigma_{y}}{\sigma_{x}}~ \quad\left[\begin{array}{l}\rho_{x, y}=\text {Pearson Correlation Coefficient} \\\sigma_{x}, \sigma_{y}=\text {Standard Deviations}\end{array} \right]$$

$$b_{0}=\bar{y}-b_{1} \bar{x}$$

Limitation of Linear Regression: Anscombe's Quartet illustrates the pitfalls of relying on pure calculation. Each graph results in the same calculated regression line > plot the distribution of residuals to see if linear regression makes sense or not. 

Example: a manager wants to find the relationship between the number of hours that a plant is operational in a week and weekly production > x: hours of operation, y: production volume 

As we expand to multiple features, an analytical solution becomes unscalable. Instead we shift focus on **minimizing** a **cost function** with **gradient descent** > we can use gradient descent to solve a cost function to calculate Beta values when we're dealing with multiple features, this can then scale to N number of features given the generalized formula. 

## Cost Functions

Until this points we discussed the following: 

- Linear relationship of x and y
- OLS: solve simple linear regression
- Not scalable for multiple features
- Translating real data to matrix notation
- Generalized formula for beta coefficients

$$\hat{y}=\sum_{i=0}^{n} \beta_{i} x_{i}$$

We decided to define a "best-fit" as the beta coefficients s.t. beta coefficients **minimize the squared error**. The residual error for some row **j** is: 

$$y^{j}-\hat{y}^{j}$$

We square the residual error and we consider the sum of squared error for m rows: 

$$\sum_{j=1}^{m}\left(y^{j}-\hat{y}^{j}\right)^{2}$$

From here we can calculate the average squared error for m rows by dividing by m: 

$$\frac{1}{m} \sum_{j=1}^{m}\left(y^{j}-\hat{y}^{j}\right)^{2}$$

This is what we need for a **cost function**. We define the following **cost function** defined by some measure of error > we want to **minimize** the cost function: 

$$\begin{aligned}
J(\boldsymbol{\beta}) &=\frac{1}{2 m} \sum_{j=1}^{m}\left(y^{j}-\hat{y}^{j}\right)^{2} \\
&=\frac{1}{2 m} \sum_{j=1}^{m}\left(y^{j}-\sum_{i=0}^{n} \beta_{i} x_{i}^{j}\right)^{2}
\end{aligned}$$

To minimize the function we take the derivative and set it equal to zero: 

$$\begin{aligned}
\frac{\partial J}{\partial \beta_{k}}(\boldsymbol{\beta}) &=\frac{\partial}{\partial \beta_{k}}\left(\frac{1}{2 m} \sum_{j=1}^{m}\left(y^{j}-\sum_{i=0}^{n} \beta_{i} x_{i}^{j}\right)^{2}\right) \\
&=\frac{1}{m} \sum_{j=1}^{m}\left(y^{j}-\sum_{i=0}^{n} \beta_{i} x_{i}^{j}\right)\left(-x_{k}^{j}\right)
\end{aligned}$$

Since this is difficult too difficult to solve analytically, we'll use gradient descent to minimize the cost function. 

## Gradient Descent

We describe the cost function through vectorized matrix notation and use gradient descent to have a computer figure out the set of Beta coefficient values that minimizes the cost / loss function. 

Goal: 

- Find a set of Beta coefficient values that minimize the error (cost function)
- Leverage computational power instead of having to manually attempt to analytically solve the derivative.

We need a beta for each feature > we can express a vector of beta values > use a gradient (sometimes referred as a multi-dimensional derivative) to express the derivative of the cost function with respect to each beta: 

$$\nabla_{\boldsymbol{\beta}} J=\left[\begin{array}{c}\frac{\partial J}{\partial \beta_{0}} \\\vdots \\\frac{\partial J}{\partial \beta_{n}}\end{array}\right]$$

$$\nabla_{\boldsymbol{\beta}} J=\left[\begin{array}{c}-\frac{1}{m} \sum_{j=1}^{m}\left(y^{j}-\sum_{i=0}^{n} \beta_{i} x_{i}^{j}\right) x_{0}^{j} \\\vdots \\-\frac{1}{m} \sum_{j=1}^{m}\left(y^{j}-\sum_{i=0}^{n} \beta_{i} x_{i}^{j}\right) x_{n}^{j}\end{array}\right]$$

We also vectorize our data: 

$$\mathbf{X}=\left[\begin{array}{ccccc}1 & x_{1}^{1} & x_{2}^{1} & \ldots & x_{n}^{1} \\1 & x_{1}^{2} & x_{2}^{2} & \ldots & x_{n}^{2} \\\vdots & \vdots & \vdots & \ddots & \vdots \\1 & x_{1}^{m} & x_{2}^{m} & \ldots & x_{n}^{m}\end{array}\right] \quad \mathbf{y}=\left[\begin{array}{c}y_{1} \\y_{2} \\\vdots \\y_{m}\end{array}\right] \boldsymbol{\beta}=\left[\begin{array}{c}\beta_{0} \\\beta_{1} \\\vdots \\\beta_{n}\end{array}\right]$$

We split the gradient up: 

$$\nabla_{\beta} J=-\frac{1}{m}\left[\begin{array}{c}\sum_{j=1}^{m} y^{j} x_{0}^{j} \\\vdots \\\sum_{j=1}^{m} y^{j} x_{n}^{j}\end{array}\right]+\frac{1}{m}\left[\begin{array}{c}\sum_{j=1}^{m} \sum_{i=0}^{n} \beta_{i} x_{i}^{j} x_{0}^{j} \\\vdots \\\sum_{j=1}^{m} \sum_{i=0}^{n} \beta_{i} x_{i}^{j} x_{n}^{j}\end{array}\right]$$

We can not calculate the gradient for any set of beta values > what is the best way to "guess" at the correct Beta values that minimize the gradient? Gradient descent! 

Process: 

- Calculate gradient at point
- Move in a step size proportional to negative gradient
- Repeat until minimum is found

This way we can leverage computational power to find optimal Beta coefficients that minimize the cost function producing the line of best fit. 

[Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)

## Coding Simple Linear Regression with Python

In this section we code a simple linear regression with Python. Afterwards, we start considering performance evaluation and multivariate regression > how can we improve linear regression. 

We limit our example one feature X > x is a vector. We will create a best-fit line to map out a linear relationship between total advertising spend and resulting sales. 

# 📚 Scikit-learn

NumPy has some built-in capabilities for simple linear regression, but when it comes to more complex models, we'll use **Scikit-Learn (sklearn)**. 

sklearn is a library containing many ML algorithms. It uses a generalized "estimator API" framework to call the ML models > the ML algorithms are imported, fitted, and used uniformly across all algorithms. 

This allows users to easily swap algorithms in and out and test various approaches > this uniform framework also means users can easily apply almost any algorithm effectively without truly understanding what the algorithm is doing! 

It also comes with many convenience tools, including train test split functions, cross validation tools, and a variety of reporting metric functions (to analyze model performance) > sklearn is a "one-stop shop" for many of our ML needs. 

Philosophy: 

- sklearn approach to model building focuses on **applying models** and **performance metrics**
- This is a more pragmatic industry style approach rather than an academic approach of describing the model and its parameters > academic users used to **R** style reporting may also want to explore the **statsmodels** python library if interested in more statistical description of models such as significance levels.

Remember the process for supervised learning: 

- Perform a Train | Test split for supervised learning: there are 4 main components X train, X test, y train, and y test (sklearn does this split (as well as more advanced cross-validation))

```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X,y) 
# this is simple tuple unpacking
```

- At the end of the supervised ML process we want to compare predictions to the y test labels

```python
from sklearn.model_family import ModelAlgo
mymodel = ModelAlgo(param1, param2) 
# we create an instance of the model and define the parameters
mymodel.fit(X_train, y_train) 
# this trains the model
predictions = mymodel.predict(X_test) 
# we predict on our X_test sample 

from sklearn.metrics import error_metric
# see later: performance evaluation techniques and what metrics are important
performance = error_metric(y_test, predictions) 
# get performance metric back
```

**This is the general framework code for essentially any supervised learning algorithm**! 

[What does "fit" method in scikit-learn do?](https://stackoverflow.com/questions/45704226/what-does-fit-method-in-scikit-learn-do)

## Linear Regression with Scikit-learn

In this section we perform a linear regression with the Scikit-learn library. 

### Data Setup and Model Training

- Data Setup
    - Reading in a data source
    - Splitting it into features and a vector label
    - Splitting it into training and test set
- Model Training
    - Creating model
    - Setting up (default) parameters
    - Training the model
- Testing the model & evaluating its performance

Expanding the question: Is there a relationship between **total advertising spend** and **sales**? > What is the relationship between **each advertising channel (TV, Radio, Newspaper)** and **sales**? 

[Random state (Pseudo-random number) in Scikit learn](https://stackoverflow.com/questions/28064634/random-state-pseudo-random-number-in-scikit-learn)

It is important when comparing ML algorithms to make sure to use the same random_state (relevant for shuffle and split). 

## Performance Evaluation with Scikit-learn - Regression Metrics

After we have a fitted model that can perform predictions based on features, how do we decide if those predictions are any good?

In this section we discuss evaluating Regression Models. Regression is a task when a model attempts to predict continuous values (unlike categorical values, which is classification task). 

Example: 

- Attempting to predict the price of a house given its features is a **regression task**
- Attempting to predict the country a house is in given its features is a **classification task** (there is no in-between value for two separate countries)

Some evaluation metrics are accuracy or recall. These sort of metrics aren't useful for regression problems since we need metrics designed for **continuous** values. 

The most common evaluation metrics for regression are: 

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Square Error (RMSE)

All of these are **loss functions** because we are trying to minimize them. 

### Mean Absolute Error (MAE)

MAE is the mean of the absolute value of the errors: 

$$\frac 1n\sum_{i=1}^n|y_i-\hat{y}_i|$$

Characteristics: 

- This is the easiest to understand since it's the average error.
- MAE won't punish large errors! See Anscombe's Quartet.

### **Mean Squared Error** (MSE)

MSE is the mean of the squared errors: 

$$\frac 1n\sum_{i=1}^n(y_i-\hat{y}_i)^2$$

Characteristics: 

- MSE is more popular than MAE, because MSE "punishes" larger errors, which tends to be useful in the real world.
- Issue with MSE: it reports back the error in different units than your original y value It reports units of y squared > really hard to interpret and explain!

### **Root Mean Squared Error** (RMSE)

RMSE is the square root of the mean of the squared errors:

$$\sqrt{\frac 1n\sum_{i=1}^n(y_i-\hat{y}_i)^2}$$

Characteristics: 

- RMSE is even more popular than MSE, because RMSE is interpretable in the y units.

Question: What is a good value for the MAE / MSE / RMSE? 

- Context is everything, e.g. $10 RMSE is fantastic for house prices, but horrible for predicting candy bar prices
- Compare error metric to the average value of the label in your data set to get an intuition of its overall performance
- Domain knowledge play an important role!
- We may create a model to predict how much medication to give > small fluctuations in RMSE may actually be very significant
- We create a model to try to improve on existing human performance > we would need some baseline RMSE to compare to and make sure we're improving on previous work

It is recommended to use both the MAE & RMSE > check to see if on average we're doing good & make sure the prediction is not far off for some data points. 

## Evaluating Residuals

[Errors and residuals](https://en.wikipedia.org/wiki/Errors_and_residuals)

It's important to separately evaluate **residuals** and not just calculate performance metrics. 

Considering Anscombe's quartet it is obvious that linear regression is not valid for every situation >  how can we tell if we're dealing with more than one x feature, whether or not linear regression was valid since we can not see this discrepancy of fit visually if we have multiple features. 

What we can do is plot residual error against true y values (scalable to any number of features) > the residual errors should be random and close to a normal distribution (centered around 0).

We can also visualize the residual plot. The **residual plot** shows residual error vs true y value. We're plotting the residual (versus y true value) > this should be random > there should be no clear line or curve! 

If Linear Regression is not valid then this will be clear in the **residual plot** as it will show a clear pattern / curve > choose another model! 

Goal: use residual plots to amke sure that the underlying ML algorithm is a valid choice. 

To make sure that the distribution of the residual is normal we can use a normal probability plot (also called QQ plot, normal quantile plot) > compare what a perfectly normally distributed data set versus your actual values (subjective normality test)

Construction: 

- Sort data ascending
- Rank the data points
- Compute Plotting Position

## Model Deployment and Coefficient

Model deployment here means only loading and saving the model for future use. Recall the supervised ML process: 

- **X and y Data > Training Data Set & Test Data Set > Fit / Train Model & Evaluate Performance >** Adjust as Needed > Deploy Model

Question: How do we adjust the model? Later, we'll explore polynomial regression and regularization as model adjustments. 

For now we focus on a simple "deployment" of our model by saving (model persistence) and loading it, then applying to new data. 

We fit the final model on all the data since we've decided that these model hyper-parameters are good enough on a test set, so when deployed to the real world, we want to take full advantage of the entire data set and retrain the model on it. 

# 🦑 Polynomial Regression

In this section we discuss Polynomial Regression (more akin to Feature Engineering and expanding a data set than creating a new model). We just completed a Linear Regression task, allowing us to predict future label values given a set of features.

Question: how can we improve on a Linear Regression Model? One approach is to consider **higher order relationships** on the feature. 

There are two main issues polynomial regression will address for us: 

- **non-linear feature relationships** to label: we're able to find accurate beta coefficients for higher orders of the feature is the relationship between the original is non-linear. Note that not every feature will have relationships at a higher order > the main point here is that it could be reasonable to solve for a single linear beta coefficient for polynomial of an original feature.
- **interaction terms between features**: what if features are only significant when in sync with one another (synergies)? Example: newspapers ads by itself is not effective, but greatly increases effectiveness if added to a TV ad campaign. Maybe consumers only watching TV  ads will create some sales, but consumers who watch TV and see a newspaper ad could contribute more sales than TV or newspaper alone. 
Question: Can we check for this? Simples way is to create a new feature that multiplies two existing features to create an **interaction term**. We can keep the original features, and add on this interaction term. sklearn does this through a **pre-processing** call.

sklearn's pre-processing library contains many useful tools to apply to the original data set **before** model training. One tool is the **PolynomialFeatures** which automatically creates both higher order feature polynomials and the interaction terms between all feature combinations. 

The features created include: 

- the bias (default value 1; indicating the y-intersect term)
- values raised to a power for each degree x**i
- interactions between all pairs of features x_i * x_j

Example for the features A and B it creates: 1, A, B, A**2, A*B, B**2 > we grab more signal from the data to determine if there are interaction term relationships or higher order relationships

## Bias Variance Trade-Off: Overfitting versus Underfitting (based on MSE)

The higher order polynomial model perform better than a standard linear regression model. How do we choose the optimal degree for the polynomial? What trade-offs are we to consider as we increase model complexity? 

In general, increasing model complexity in search for better performance leads to a **bias-variance trade-off.** We want to have a model that can generalize well to new unseen data, but can also account for variance and patterns in the known data. 

Extreme bias or extreme variance both lead to bad models. We can visualize this effect by considering a model that underfits (high bias) or a model that overfits (high variance). 

Overfitting:

The model fits too much to the noise from the data. This often results in **low error on training sets** but **high error on test / validation sets** > the model performs well on the training set and bad on unseen data (test or validation set).

Underfitting:

Model does not capture the underlying trend of the data and does not fit the data well enough. Low variance but high bias. Underfitting is often a result of an excessively simple model. 

Model has high bias and is generalizing too much. Underfitting can lead to poor performance in both training and testing data sets.  

It is easy to visualize if the model is over- or underfitting in one dimension, but what do we do in multi-dimensional data sets? Assume we train a model and measure its error versus model complexity, e.g. higher order polynomials > we plot the **error versus model complexity**. Both these quantities scale regardless of how many features we have. 

When thinking about over- and underfitting we want to keep in mind the relationship of model performance on the training set versus the test / validation set. If we overfit on the training data, we will perform poorly on the test data. Ideally, the curve for the train set will be a falling convex curve. 

Process: 

- Check performance on the **training set** (x: model complexity, y: error).
- Check performance on the **test set** (to avoid overfitting on the train set).
    - If the model is not overfitted both curves will run similarly, i.e. both will be falling convex curves
    - If the model is overfitted to training data then with increasing model complexity the error will increase rapidly after a certain point > decide on a cut-off point (of model complexity)

When deciding optimal model complexity **and** wanting to fairly evaluate our model's performance , we can consider both the train error and test error to select an ideal complexity. 

In case of Polynomial Regression complexity directly relates to degree of the polynomial. Other ML algorithms have their won hyper-parameters that can increase complexity, .e.g. in random forest the amount of decisions trees. 

For choosing the optimal model complexity (order polynomial), we will need to understand error for both training and test data to look out for potential overfitting. See also this [article](https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229#:~:text=Variance%20is%20the%20variability%20of,it%20hasn't%20seen%20before.) and [question](https://datascience.stackexchange.com/questions/80157/what-are-bias-and-variance-in-machine-learning) (both may have some mistakes!)

$$\begin{aligned}\mathbb{E}\left[\left(\hat{\theta}_{S}-\theta\right)^{2}\right] &=\mathbb{E}\left[\hat{\theta}_{S}^{2}\right]+\theta^{2}-2 \mathbb{E}\left[\hat{\theta}_{S}\right] \theta \\\operatorname{Bias}^{2}\left(\hat{\theta}_{S}, \theta\right) &=\left(\mathbb{E}\left[\hat{\theta}_{S}\right]-\theta\right)^{2} \\&=\mathbb{E}^{2}\left[\hat{\theta}_{S}\right]+\theta^{2}-2 \mathbb{E}\left[\hat{\theta}_{S}\right] \theta \\\operatorname{Var}\left(\hat{\theta}_{S}\right) &=\mathbb{E}\left[\hat{\theta}_{S}^{2}\right]-\mathbb{E}^{2}\left[\hat{\theta}_{S}\right]\end{aligned}$$

# 🍡 Regularization and Cross Validation

In this section we discuss different types of regularization and related topics. Regularization is the process of adding information in order to solve an ill-posed problem or to prevent overfitting

Regularization seeks to solve a few common model issues by: 

- minimizing model complexity
- penalizing the loss function
- reducing model overfitting (add more bias to reduce model variance)

In general, we can think of regularization as a way to reduce model overfitting and variance: 

- requires some additional bias
- requires a search for optimal penalty hyper-parameter

Three main types of Regularization: 

- L1 Regularization
    - LASSO Regression
- L2 Regularization
    - Ridge Regression
- Combining L1 and L2
    - Elastic Net

**L1 Regularization** 

L1 Regularization adds a penalty equal to the **absolute value** of the magnitude of coefficients (**RSS:** Residual Sum of Squares): 

- Limits the size of the coefficients
- Can yield sparse models where some coefficients can become zero

Minimize the following function (we can tune the hyper-parameter lambda): 

$$\sum_{i=1}^{n}\left(y_{i}-\beta_{0}-\sum_{j=1}^{p} \beta_{j} x_{i j}\right)^{2}+\lambda \sum_{j=1}^{p}\left|\beta_{j}\right|=\operatorname{RSS}+\lambda \sum_{j=1}^{p}\left|\beta_{j}\right|$$

**L2 Regularization** 

L2 Regularization adds a penalty equal to the square of the magnitude of coefficients: 

- All coefficients are shrunk by the same factor
- Does not necessarily eliminate coefficients

Minimize the following function (we can tune the hyper-parameter lambda): 

$$\sum_{i=1}^{n}\left(y_{i}-\beta_{0}-\sum_{j=1}^{p} \beta_{j} x_{i j}\right)^{2}+\lambda \sum_{j=1}^{p} \beta_{j}^{2}=\mathrm{RSS}+\lambda \sum_{j=1}^{p} \beta_{j}^{2}$$

**Combining L1 and L2**

Elastic Net combines L1 and L2 with the addition of an alpha parameter deciding the ratio between them (alpha = 0 > we don't consider L1, alpha = 1 > we don't consider L2): 

$$\frac{\sum_{i=1}^{n}\left(y_{i}-x_{i}^{J} \hat{\beta}\right)^{2}}{2 n}+\lambda\left(\frac{1-\alpha}{2} \sum_{j=1}^{m} \hat{\beta}_{j}^{2}+\alpha \sum_{j=1}^{m}\left|\hat{\beta}_{j}\right|\right)$$

These regularizations methods do have a cost:

- Introduce an additional hyper-parameter that needs to be tuned (guess & check)
- This hyper -parameter can be thought of as a multiplier to the penalty to decide the "strength" of the penalty

We will cover L2 regularization (Ridge Regression) first, because to the intuition behind the squared term being easier to understand. Before coding regularization we need to discuss Feature Scaling and Cross Validation. 

## Feature Scaling and Regularization

[Feature scaling](https://en.wikipedia.org/wiki/Feature_scaling)

Feature scaling provides many benefits to our ML process. Some ML models that rely on distance metric, e.g. KNN, **require** feature scaling to perform well. 

Feature scaling improves the convergence of steepest descent algorithms, which do not possess the **property of scale invariance**. If features are on different scales, certain weights may update faster than others since the feature values x_j play a role int he weight updates. 

Critical benefit of feature scaling related to gradient descent. There are some ML algos where scaling won't have an effect, e.g. CART (regression, decisions trees, random forests > decisions tree based algorithms) based methods

Scaling the features so that their respective range are uniform is important in comparing measurements that have different units. It allows us to directly compare model coefficients to each other. 

Caveats: 

- must always scale new unseen data before feeding to model
- affects direct interpretability of feature coefficients: easier to compare coefficients to one another, but harder to relate back to original unscaled feature > it's a trade-off between being able to compare coefficients between each other versus being able to relate coefficients to the original unscaled feature

Benefits: 

- Can lead to great increases in performance
- Necessary for some models
- Virtually no "real" downside to scaling features

Two main way to scale features: 

- **Standardization** (also referred as Z-score normalization): rescales data to have a mean or 0 and a standard deviation of 1: X_s = (X - X.mean()) / X.std()
- **Normalization**: Rescales all data values to be between 0 and 1: X_m = (X - X.min()) /( X.max() - X.min())

There are other methods of scaling features and sklearn provides easy to use classes that "fit" and "transform" feature data for scaling: 

- a .fit() method call calculates the necessary statistics, e.g. X_min, X_max, X_mean, X_std, etc.
- a .transform() method call actually scales data and returns the new scaled (transformed) version of the data

Note that in the previous section we created new features and populated the columns, we did **not** scale the data! Important considerations for fit and transform: 

- Only **fit** to training data! Calculating statistical information should only come from training data since we don't want to assume prior knowledge of the test set!
- Using the full data set would cause **data leakage**: calculating statistics from full data leads to some information of the test set leaking into the training process upon transform() conversion.

Feature scaling **process**:

- perform train test split
- fit to training feature data
- transform training feature data
- transform test feature data
- (make predictions**)**

We do **not** scale the label! It's not necessary nor advised. Normalizing the output distribution is altering the definition of the target. Predicting a distribution that doesn't mirror your real-world target. Additionally, it can negatively impact stochastic gradient descent (see [article](https://stats.stackexchange.com/questions/111467/is-it-necessary-to-scale-the-target-value-in-addition-to-scaling-features-for-re)). 

## Cross Validation

See Section 5.1 of ISLR. Cross validation is a more advanced set of methods for splitting data into training and testing sets. Cross-validation is a resampling procedure used to evaluate machine learning models on a limited data sample. 

We understand the intuition behind performing a train test split, we want to fairly evaluate out model's performance on unseen data > we are **not** able to tune hyper-parameters to the **entire** dataset. 

Question: can we achieve the following: 

- train on all the data and
- evaluate on all the data?

We can achieve this with cross validation. 

### Principle

We split the data into k equal parts (axis = 0) > we have the ratio 1/k left as test set. We train the model and get the error metric for split. We repeat this process for all possible splits and determine error_1, ..., error_k. We computer the mean error > the average error is the expected performance. 

We were able to train on all data **and** evaluate on all data (the caveat being that we did not do it all at once, but over k times) > we get a better sense of true performance across multiple potential splits. What is the cost of this? We have to repeat computations k number of times! 

This is known as k-fold cross-validation. Common choice for k is 10 so each test set is 10% of your total data. Largest k possible would be the #rows-1. This is knows as *leave one out* cross validation; gives us a good sense of the model's performance but computationally expensive. 

### Hold Out Test Set

One consideration to note with k-fold cross validation and a standard train test split is fairly tuning hyper-parameters. If we tune hyper-parameters to test data performance, are we ever fairly getting performance results? Does this constitute data leakage? 

How can we understand how the model behaves for data that is has not seen **and** not been influenced by for hyper-parameter tuning? For this we can use a **hold out** test set. 

We fold the data set and remove a hold out test set. The model will not see this data **and** never be adjusted to. At this point we have two options: 

1. Train and tune on this data
2. Perform k-fold cross validation, train, and tune on this data 

After training and tuning perform **final evaluation** on hold out test set. We can **not** tune after this final test evaluation! The idea being that we want a performance metric as a final report how we'll the model is going to perform based on data that it was not trained on **and** based on data that it was never adjusted to. The new split names become: 

**Train | Validation | Test Split** > allows us to get a true final performance metric to report (no editing model after test!) 

Note that all the approaches discussed above are valid, each situation is unique. Keep in mind: 

- previous modeling work
- reporting requirements
- fairness of evaluation
- context of data and model

The most robust approach would be a k-fold cross-validation with a holdout test set. 

Many regularization methods have tunable parameters we can adjust based on cross-validation techniques. 

### Regularization Data Setup

Process: 

- import numpy, pandas, matplotlib.pyplot, and seaborn
- read in data, assign data to matrix, vector
- polynomial conversion (generate polynomial features)
- split data into train and test data set
- standardize the data (avoid data leakage!)

## L2 Regularization - Ridge Regression

Start here! 

# 🔧 Open Questions and Tasks

## Open Questions

- What are our categorical columns to group by?
- Do we need to use datetime objects in our project?

## Backlog

- Logistics Regression
- Machine Learning
- Revise the lecture before the presentation!
- Read about [copy warning](https://realpython.com/pandas-settingwithcopywarning/)
- Read Wiki on [Regression Analysis](https://en.wikipedia.org/wiki/Regression_analysis)

## In Progress

- Linear Regression
- Convert [rawTimesamp](https://stackoverflow.com/questions/19231871/convert-unix-time-to-readable-date-in-pandas-dataframe) feature into a datetime object > useful later for feature engineering (see [documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html))
- Make an outline of the project
- Decide what are the relevant categorial columns for the project
- Make a [data column reference](https://www.notion.so/ac02bfefe61246918aabf0e6094f18c9) in HTML (see [data type](https://en.wikipedia.org/wiki/Data_type), [7 data types](https://towardsdatascience.com/7-data-types-a-better-way-to-think-about-data-types-for-machine-learning-939fae99a689); use Notion or [Tables Generator](https://www.tablesgenerator.com/html_tables))
- Strip project data
- Determine an average payload

## Resolved (Preparation)

- Crapstone Project (Numpy, Pandas, Matplotlib, and Seaborn)
- Seaborn
- Matplotlib
- Pandas
- Numpy
- Machine Learning Pathway
- Python Crash Course
- Upload files to Github
- Do crash course on Git

## Resolved (Project)

- Make sure there is no missing data in the project

## Workflow

- pull repo (T)
- work on project (N, J)
- update readme (N, F, T, VS)
    - export readme (N)
    - rename and replace old readme (F)
    - generate TOC (T)
    - remove metadata (VS)
    - save to HTML (VS)
- push repo (T)

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

[pandas - check for non unique values in dataframe groupby](https://stackoverflow.com/questions/33732106/pandas-check-for-non-unique-values-in-dataframe-groupby)

[How to install the JupyterLab plugin](https://help.kite.com/article/143-how-to-install-the-jupyterlab-plugin)

[Meaning of 'hue" in seaborn barplot](https://datascience.stackexchange.com/questions/46117/meaning-of-hue-in-seaborn-barplot)

[Six easy ways to run your Jupyter Notebook in the cloud](https://www.dataschool.io/cloud-services-for-jupyter-notebook/)

[Add percentages instead of counts to countplot · Issue #1027 · mwaskom/seaborn](https://github.com/mwaskom/seaborn/issues/1027)

[Python: Plotting percentage in seaborn bar plot](https://stackoverflow.com/questions/35692781/python-plotting-percentage-in-seaborn-bar-plot)

[How to deal with SettingWithCopyWarning in Pandas](https://stackoverflow.com/questions/20625582/how-to-deal-with-settingwithcopywarning-in-pandas)

[Select by partial string from a pandas DataFrame](https://stackoverflow.com/questions/11350770/select-by-partial-string-from-a-pandas-dataframe)

[SettingWithCopyWarning in Pandas: Views vs Copies - Real Python](https://realpython.com/pandas-settingwithcopywarning/)

[pandas.DataFrame.copy - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.copy.html)

[Indexing and selecting data - pandas 1.1.5 documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html)

[why should I make a copy of a data frame in pandas](https://stackoverflow.com/questions/27673231/why-should-i-make-a-copy-of-a-data-frame-in-pandas)

[return string with first match Regex](https://stackoverflow.com/questions/38579725/return-string-with-first-match-regex)

[Creating for loop until list.length](https://stackoverflow.com/questions/14532875/creating-for-loop-until-list-length)

[IPython Notebook cell multiple outputs](https://stackoverflow.com/questions/34398054/ipython-notebook-cell-multiple-outputs)

[sklearn: how to get coefficients of polynomial features](https://stackoverflow.com/questions/31290976/sklearn-how-to-get-coefficients-of-polynomial-features)