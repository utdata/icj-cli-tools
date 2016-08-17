Personal notes on Pandas
=========================

I've been using the [ModeAnalytics tutorial](https://community.modeanalytics.com/python) on Python to learn a bit about [pandas](https://community.modeanalytics.com/python/libraries/pandas/), and considering using it in class.

### to get SQL query in notebook

Run the query, then pull into a notebook with this:

`data = datasets[0]`

Now `data` is my variable. I *think* that puts it into a dataframe.

#### Fill nulls
If there are blank cells:

`data = data.fillna('') # replace missing values with ''`

### import Pandas

`import pandas as pd`

*I think the `.plot` command is pandas, but I'm not sure. `.value_counts` as well.*

### head command

To peek at the data:

`data.head()`

### Get a column
`data['column_name']`

### get a row

`data.ix[0]`

### count

To get a count of values of a items in a column:

`data['column'].value_counts()[:20] #get the top 20`

### plot

To get that count into a quick bar chart, add on `.plot(kind='barh')`
