

```text
## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

Sam Bail: Tutorial Intro to Jupyter Notebook and Data Analysis with Pandas

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2021/29-sam-jupyter-pandas.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/278956168/
- Video:  https://youtu.be/hc8-AhYBu08
- GitHub repo:   https://github.com/spbail/pandas-and-jupyter-workshop

## Outline
- Intro and Background
- Part 0: Quick Jupyter tutorial
- Part 1: Loading and inspecting data
- Part 2: Data cleaning
- Part 3: Data analysis
- Part 4: Summary

## Agenda
00:00:00 Reshama introduces Data Umbrella
00:03:33 Sam begins presentation 
00:04:40 Jupyter notebook presentation begins, use Binder or run Jupyter notebook locally
00:07:30 Jupyter Notebook: navigating the notebook browser
00:07:52 Outline of talk
00:10:40 What is Jupyter and the whole Jupyter Ecosystem? (IPython, Jupyter, JupyterLab, Binder)
00:13:00 JupyterLab
00:14:40 What is pandas / matplotlib / pyplot / seaborn?
00:17:30 Part 0: Quick Jupyter Tutorial (10 minutes) 
00:22:37 Cell magic in Jupyter Notebook (%time, %%time)
00:25:25 Part 1: Loading and inspecting the data
00:25:55 Load data from a csv file
00:26:48 About Dataframes
00:29:57 Inspecting a dataframe using built-in functions: .info, .head, .sample, .describe
00:34:50 Accessing columns in a dataframe
00:41:08 Accessing rows in a dataframe ( Using .loc function in python)
00:46:45 Sorting dataframes: .sort_values
00:49:44 Sorting with `inplace` parameter: df.sort_values[('columnA'), inplace=True]
00:52:20 Part 2: Data cleaning
00:53:15 Date conversion (object, data type): pd.to_datetime      
00:56:05 Part 3: Data analysis
00:57:10 Checking for duplicate records: df['columnA'].unique()
00:58:05 groupby: df.groupby('columnA').count() ; df.groupby('columnA').nunique()
01:02:10 Indexes in dataframes
01:03:20 df.groupby('columnA').count()[['columnB]].reset_index
01:08:15 Plotting data from dataframe
01:11:42 Changes to treatment data over time (datetime)
01:21:00 Question on pivot table in pandas 
01:22:35 Question on pivotting a table definition
 
## Event

This talk is aimed at Python users with no prior knowledge of Pandas. In this talk, we will explore a small dataset and introduce you to the basics of data analysis workflows using the Pandas library and Jupyter notebook. We will show how to to load data from a CSV file, do some basic exploratory data analysis and data cleaning, generate simple statistics, and create some basic data visualizations.

## About the Speaker

Sam Bail (http://www.sambail.com) is a data professional in New York City with a passion for turning high quality data into valuable insights. Sam holds a PhD in Computer Science and has worked for several data-centric startups.

LinkedIn: https://www.linkedin.com/in/spbail
Twitter:https://twitter.com/spbail
GitHub: https://github.com/spbail


```
