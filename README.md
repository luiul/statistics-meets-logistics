# Statistics Meets Logistics - Python for Data Science and Machine Learning

Categories: https://www.notion.so/Uni-6f742c040da1488181ef1078d9bac25c, https://www.notion.so/Priv-186a1091f6eb44aba651be4262aee091, https://www.notion.so/Prof-5875739d08f346a2a1807f06823d4ab4
Comment: 3 ECTS Credits 
Date Created: Nov 27, 2020 3:36 PM
Prio: High
Status: Active

# Statistics Meets Logistics

The [course](https://www.statistik.tu-dortmund.de/2791.html) and the [material](https://moodle.tu-dortmund.de/enrol/index.php?id=22199) provided by the lecturer are in German. The documentation is in English.

## Description

In the course, students will learn about the application of statistical methods and basic machine learning procedures for the analysis of complex data in the field of logistics. This includes methods of descriptive statistics as well as various regression and classification procedures including neural networks. After the introduction of the methods, the students apply the acquired knowledge independently to work on logistical problems in various practical exercises. The software Python and relevant packages are used.

# Background

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

# Python Crash Course

This is the section for the Python crash course. [Current Python documentation](https://docs.python.org/3/contents.html).

## Crash Course

If a variable is being highlighted by the IDE, this keyword is reserved for an object!

- String interpolation / [.format()](https://pyformat.info/) on string = a way to insert things into a string
- List = arrays in other languages. In Python a list can contain objects of different types. Lists can be nested (useful with 2D object, e.g. a matrix). Important function:
    - list(iterable) is a list constructor.
    - Append: Adds its argument as a single element to the end of a list. The length of the list increases by one
    - extend(): Iterates over its argument and adding each element to the list and extending the list. The length of the list increases by number of elements in it’s argument
- Dictionaries = hash tables in other languages. Dictionaries do not retain any order! Important function: update([other])
- Truthy and Falsy values: Python treat the following values as False: `"", 0, 0.0, 0j, [], (), {}, False, None, instances which signal they are empty`
- Tuples are immutable
- Sets: unordered collection of unique elements
- Range `range()`: iterate though elements of range 0, ... , arg or create a list with the elements of the range
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

# Machine Learning Pathway

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

Real World > Collect & Store Data <> Data Analysis > Machine learning models > Real World

C**ollect & Store Data** (Role: Data Engineer):

- Raw Data: data from physical sensors, surveys, simulation, experiments, data usage, etc.
- Process & Store Data: SQL database, CSV files, Excel files, cloud storage, etc.

Data Analysis (Role: Data Analyst or Data Scientist)

- **Clean & Organize Data**: reorganize data, dealing with missing data, restructure data, etc.
- Overlap with Collect & Store Data: reorganize data, dealing with missing data, restructure data, etc.
- **Exploratory Data Analysis**: statistical analysis (e.g. hypothesis test) and visualizations
- Create: report, visualization or communication > Answer question by understanding different trends and visualizations > Make  decision & Answer key questions

Machine Learning Models (Role: Data Scientist or Machine Learning Engineer)

- Supervised Learning: Predict a future outcome (based on labeled historical data)
- Unsupervised Learning: Discover hidden patterns in data
- Create: service, dashboard, application, etc > data product (predict future outcomes or gain insight on data) > Affect some change in the real world

# NumPy

NumPy is a Python library. Almost every data science library is built using NumPy.

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

# Open Questions and Tasks

## Open Questions

- Can we model the process in the project as a Poisson process?

## Backlog

- Do crash course on Git
- Upload files to Github
- Start with statistical tools
- Watch [collaboration in Git and Jupyter notebook](https://www.youtube.com/watch?v=J3k3HkVnd2c) for ideas
- Pandas
- Matplotlib
- Seaborn
- Crapstone
- Linear Regression
- Logistics Regression
- Machine Learning

## In Progress

- Numpy

## Resolved

- Python Crash Course
- Machine Learning Pathway

# Misc

- $PATH is stored in /etc/paths; open with sudo nano to modify
- [Check if word in in a string](https://stackoverflow.com/questions/5319922/python-check-if-word-is-in-a-string)