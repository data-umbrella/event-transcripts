# Kimberly Fessel: Polars for Data Analysis in Python

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2024/105-kimberly-polars.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/302970786
- Video: https://youtu.be/5V_MvnwTVwc
- Transcriber:  ? [needs a transcriber]

## Resources
- Repo: bit.ly/DUPolars (https://github.com/kimfetti/Conferences/tree/master/DataUmbrella_2024)
- Slides: https://github.com/kimfetti/Conferences/blob/master/DataUmbrella_2024/DataUmbrella_2024_KFessel_Deck.pdf
- Kimberly Fessel's YouTube: https://www.youtube.com/c/kimberlyfessel
- To learn more about Rust, check out this video: https://youtu.be/7E8nLExn3WI
- Save the date: Nov 19, 2024, We have another polars event: Understanding Polars Expressions when you're used to pandas
- Polars on GitHub: https://github.com/pola-rs/polars

## About the Event
Discover Polars, the high-performance DataFrame library revolutionizing data analysis in Python. Built on Rust, Polars offers unparalleled speed and efficiency, outperforming pandas, Dask, and even PySpark. Explore its innovative features like lazy evaluation, memory efficiency, and automatic multi-threading, designed to handle large datasets with ease.

In this session, you'll learn practical techniques for data manipulation and advanced transformations. We will demonstrate Polars' syntax and capabilities, making it accessible even if you’re new to Polars. Join us to elevate your Python data analysis to the next level.
This presentation covers:

- Section 1: What is Polars and how does it compare to pandas?
- Section 2: Getting Started with Polars in Python
- Section 3: Advanced Data Analysis with Polars
- Section 4: Should you switch to Polars?

```
## Timestamps
00:00 Data Umbrella introduction
04:15 Kim begins talk; about Kimberly Fessel
06:17 What is Polars?
07:40 Polars is built on Rust
08:55 Polars development and adoption
09:46 Key features of polars (speed)
13:11 Lazy evaluation
15:56 Q&A: What architecture were the speed tests run on?
16:50 Q&A: How is it able to achieve multi-threading since Python has an interpreter lock?
17:35 Polars vs Others (pandas, PySpark, SQL), syntax
19:15 Polars compared with Pandas: similarities
20:06 Polars compared with Pandas: differences (index names, parallelism, lazy evaluation, better syntax)
21:40 Polars compared with Dask
22:55 Polars compared with Apache Spark
24:30 Getting started with Polars in Python: installation, Jupyter notebook
27:20 break: fix tech issue
28:22 back to Jupyter notebook with Python demo
30:20 Q: Can you clarify what size datasets are for Polars?
31:17 Q: Does Polars have “series” concept as in pandas?
31:37 Q: Understanding multi-processing in polars
32:30 back to Jupyter notebook: exploring polars dataframe (sampling and more)
33:20 select() columns
34:30 filter() data
36:45 Adding new columns; computing new columns
38:40 .alias() new column name
39:50 Polars can create columns in parallel for speedier calculations
41:32 Advanced operations in polars (missing data, join dataframes, analysis
42:38 Notebook 2: Advanced Data Analysis with Polars
43:00 lazy evaluations: pl.scan_csv()
46:10 Advanced examples of Polars code
49:33 Q: Does Polars have the pandas feature in_place=True?
50:14 Q: What are the options for plotting data in Polars?
50:35 Explore more advanced options: transformations, SQL queries, user-defined functions
51:25 Data visualization, plotting in Polars
53:32 Converting to pandas
54:30 Should you switch to Polars?
54:40 Other data source options: Excel, parquet, JSON, database
54:58 Working with large files: lazy evaluation, streaming data
55:51 Advanced operations
56:17 When should I use polars?
58:32 Resources
01:00:00 Q: Can we use Polars as input data into scikit-learn, or do we need to convert to pandas or NumPy first?
01:00:00 Upcoming meetup on Nov 19, 2024:  Understanding Polars Expressions When You Are Used to pandas (https://www.meetup.com/data-umbrella/events/)
01:01:22 Q: Do you now use Polars exclusively or do you still use pandas?
01:02:45 Q: When you make a copy of a dataframe, is it still a shallow copy?
01:03:05 Q: Any disadvantages to using Polars?
01:04:15 Q: Should I learn Polars instead of pandas?
```
https://github.com/data-umbrella/event-transcripts/issues/92


## About the Speaker
Kimberly Fessel is a data scientist and the founder of Dr Kim Data. She and her company specialize in technical instruction, machine learning, and data visualization. Kimberly has over a decade of experience educating groups and individuals in corporate settings, at academic universities, via online platforms, and as director of a data science bootcamp. Her educational YouTube channel features videos about data science in Python and boasts over 20,000 subscribers. Kimberly holds a PhD in applied mathematics from Rensselaer Polytechnic Institute and expects the publication of her first book, Head First SQL, 2nd Edition, in 2026.

- LinkedIn: https://www.linkedin.com/in/kimberlyfessel/

#DataScience #DataAnalysis


## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=5V_MvnwTVwc" target="_blank"><img src="http://img.youtube.com/vi/5V_MvnwTVwc/0.jpg"
alt="Polars for Data Analysis in Python" width="50%" /></a>

## Transcript
