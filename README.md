# Learning Pandas 
It is a Python library to analyse data.

## Data Structures in Pandas
* **Series** 

    It is a 1D ndarray with axis labels(i.e. index). It can accept:
    - Python dict
    - ndarray
    - A scalar value(like 5)

* **Dataframes** 

    It is 2D labelled data structure with columns of potentially different types. It can accept:
    - Dict of 1d ndarrays, lists, dicts, or series
    - 2d ndarray
    - `Series`
    - `Dataframe`

We will learn:
- Creating rows and columns in dataframes
- Deleting rows(i.e index, temporary/permanently)- using `drop()`
- Accessing elements- `df[]` for columns and `df.loc[]` for rows
    - conditional accessing
- Analysing data using groupby()
- Joining
- Concatenation- (it appends Dataframe)
- Merging
- More operations such as:
    - `index()`- returns info about index of dataframe
    - `columns()`- returns info about columns of dataframe
    - `apply(fun)`- appplies function '`fun()`' on the dataframe
    - `sum()`- returns sum
    - `sort_values(by=)`- sorts values in acsending order
    - `unique()`- returns unique elements of any column
    - `nunique()`- returns number of unique elements of any column
    - `value_counts()`- returns count of thos unique elements
    - `isnull()`- returns boolean value `True` if any data is not available, otherwise `False` 

# Difference between Join, Concatenation and Merging

Join | Concatenation | Merging
--- | --- | ---
|used to join two or more pandas Dataframes/Series horizontally |concatenate two or more pandas Dataframes/Series vertically or horizontally| used to merge Dataframe with database-style join. Combining exactly two Dataframes
|aligns calling dataframes column(s) or index with other objects' index(and not the columns)| aligns only the index by specifying axis parameter|if joining columns-on-columns Dataframe indexes will be ignored
|uses merge internally for index-on-index or column(s)-on-index join|- |-
|Defaults to left join|Defaults to outer join |-