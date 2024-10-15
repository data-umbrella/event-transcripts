# Pablo Duboue: RAGged Edge Box: A Personal AI-Powered Document Search System

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2024/106-pablo-rag.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/303430325/
- Video: 
- Transcriber:  ? [needs a transcriber]

## Resources
- https://textualization.com/ragged/

## About the Event
One of the most popular embodiments of Generative AI are information retrieval (IR) augmented generation (RAG). Such systems use an information retrieval engine (based on semantic embeddings or keyword search) and then use a Large Language Model (LLM) to extract answers to a given query.

These systems require a large amount of computation and are usually implemented in the cloud which presents data privacy issues.

In this talk we will present The RAGged Edge Box project in which basic embedding systems and small local LLMs are packaged inside a multi-platform virtual machine (VirtualBox). The system provides a Web interface that runs locally and allows access to the RAG functionality in a completely private manner. The neural networks run on a ONNX runtime and do not require a GPU. RAG code is implemented in PHP and is easy to modify, requiring a much smaller execution environment than a Python alternative.
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
Dr. Duboue is an independent language technologist. His work focuses on applied language technology and natural language generation. He received a Licenciatura en Computacion degree from Cordoba University (Argentina) in 1998 and M.S., M.Phil and Ph.D. degrees in Computer Science from Columbia University in the City of New York in 2001, 2003 and 2005. He is passionate about improving society through language technology and splits his time between teaching, doing research and contributing to free software projects. He has taught at Cordoba University, Columbia University, Siglo21 University and has worked for IBM TJ Watson Research as a Research Staff Member.

- LinkedIn: https://www.linkedin.com/in/pabloduboue/

#NaturalLanguageProcessing #Machinelearning #GenAI #RAG


## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=5V_MvnwTVwc" target="_blank"><img src="http://img.youtube.com/vi/5V_MvnwTVwc/0.jpg"
alt="RAGged Edge Box: A Personal AI-Powered Document Search System" width="50%" /></a>

## Transcript
