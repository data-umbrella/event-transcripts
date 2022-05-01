```text
## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

Sean Law: Modern Time Series Analysis with STUMPY

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2021/30-sean-stumpy.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/278955616/
- Video:  https://youtu.be/XKNdXN-Jfmo

## Resources
- Documentation: https://stumpy.readthedocs.io/en/latest/
- STUMPY on Twitter: https://twitter.com/stumpy_dev

## Agenda
00:00:00 Reshama introduces Data Umbrella
00:04:07 Sean begins talk 
00:05:14 The time series business problem
00:08:00 Overview: Visualizations, Statistics, ARIMA, Anomaly Detection, Forecasting, Machine Learning, Clustering, Dymamic Time Warping
00:10:00 Deep Learning
00:11:38 Simple dataset example: Time series with length, n=13 (look for repeat patterns, anomalies)
00:12:20 Subsequence: a portion or section of the full time series
00:12:55 What's the goal in analyzing time series data?
00:13:30 Question: Do any conserved behaviors exist in my time series data?
00:13:50 Occam's Razor: simpler solutions are more likely to be correct than complex ones
00:14:15 Simple and intuitive approaches to analyzing time series data: easy to interpret, user/data agnostic, no prior knowledge, parameter free (or limited)
00:15:55 Parameters to choose: subsequence length m
00:16:20 Using Euclidean distance to compare two subsequences (Pythagorean Theorem)
00:18:40 Pairwise Euclidean Distance (distance profile: closest match, nearest neighbor)
00:21:00 computing distance matrix: gives full information about conservation of subsequences
00:22:12 Question to consider: is this solution scalable?
00:22:25 compute distance matrix using python
00:24:57 a new data structure: matrix profile.  "Matrix Profile" papers published in 2016 by University of California at Riverside & University of New Mexico
00:25:23 What is a matrix profile? A: A vector that stores the distance between each subsequence within a time series and its nearest neighbor
00:27:40 looking at global minima (subsequence are each other's nearest neighbors) (motif = potential pattern)
00:29:00 matrix profile index = the index (location) of the nearest neighbor for a given subsequence
00:30:30 global, maxima, discord, anomaly
00:31:10 Brute force, STAMP, STOMP, GPU-STOMP





## Event
STUMPY is a powerful and scalable library that efficiently computes something called the matrix profile, which can be used for a variety of time series data mining tasks.

## About the Speaker
Sean Law is a senior applied scientific researcher and lead data scientist currently working with a multi-talented R&D team at Charles Schwab. He has experience producing cutting edge methodologies, building high-performance predictive models, and developing rapid prototypes. Additionally, he is one of the co-organizers of PyData Ann Arbor and is also the creator and core maintainer of STUMPY, a powerful and scalable open source Python library that can be used for a variety of time series data mining tasks..

Linkedin: https://www.linkedin.com/in/seanlawphd/
Twitter: https://twitter.com/seanmylaw
GitHub: https://github.com/seanlaw


```
