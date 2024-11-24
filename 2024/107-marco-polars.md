# Marco Gorelli: Polars & Narwhals: Understanding Expressions When You're Used to pandas

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2024/107-marco-polars.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/304005848
- Video: https://youtu.be/kPtUPe5Egak
- Transcriber:  ? [needs a transcriber]

## Resources
- Polars documentation: https://docs.pola.rs/
- Narwhals: https://narwhals-dev.github.io/narwhals/
- Slides:  https://github.com/data-umbrella/event-transcripts/blob/main/resources/polars-narwhals.pdf
- Video: Polars for Data Analysis in Python:  https://youtu.be/5V_MvnwTVwc

## About the Event
When it comes to dataframes, pandas is the go-to library for many people. Yet Polars is taking the world by storm, and so many data practitioners are curious about trying it out. There is a learning curve though, as Polars introduces some concepts which pandas users might not be familiar with. This talk will be a deep dive into one of those concepts (expressions) and will focus on how you can understand them from a pandas perspective.

The lessons learned will be useful beyond Polars, as they will also enable you to use Narwhals. Narwhals is a lightweight and extensible compatibility layer between dataframe libraries which is gaining traction (Altair, Marimo, scikit-lego, and more are currently using it) - like Polars, its API is also based on expressions. By learning this concept, you will not only be able to use Polars efficiently, but you'll also know how to build dataframe-agnostic tools.

```
## Timestamps
00:00 Data Umbrella introduction
05:07 Marco begins presentation
06:15 Timeline / Agenda of presentation
07:15 Why care (about Polars)?
08:05 Polars crash course
08:10 -- DataFrame
09:02 -- Series
09:38 -- Expressions
10:28 Expressions: a light introduction / selection
11:18 Functions: a detour
13:10 scikit-learn uses Polars in some of their documentation
13:53 Expressions: multiple inputs (and outputs)
16:35 Expressions: summary
17:15 What about group-by aggregations?
18:20 pl.col(‘weight’).sum() (data type is preserved)
18:47 Expressions in group-by
20:05 pandas syntax comparison
21:05 Expressions: can we use them in pandas
23:20 Should pandas adopt the expressions in pandas? Let us know.
23:30 Narwhals
25:05 Conclusion
26:49 Q: Do polars expressions support Python type annotations?
27:35 Q: If I start a new project, should I use Polars and not pandas?
28:58 Q: What size datasets can I use for Polars? Streaming in Polars
30:03 Q: Is Narwhals a way to provide an array API equivalent for dataframes?
31:20 Q: How is it able to achieve multi-threading?
33:00 Q: Could we use Polars as input to scikit-learn?
33:15 Q: When you make a copy of a dataframe, is it still a shallow copy?
33:48 Q: Any disadvantage to using Polars?
34:25 Q: Should I learn Polars instead of pandas?
```

https://github.com/data-umbrella/event-transcripts/issues/92


## About the Speaker
Marco is a core dev of pandas and Polars and author of Narwhals. He's spoken at several Python conferences, taught Polars professionally, and written the first complete Polars plugins tutorial. He currently works as Senior Software Engineer at Quansight Labs.

Before getting involved in open source software, he worked in data science and was one of the prize winners of the M6 forecasting competition. He's an advocate for making it more accessible to contribute to open source software and has run several mentored sprints, aimed both at the general public and at underrepresented groups in tech.

- LinkedIn: https://www.linkedin.com/in/marcogorelli/

#DataScience #OpenSource #MachineLearning


## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=kPtUPe5Egak" target="_blank"><img src="http://img.youtube.com/vi/kPtUPe5Egak/0.jpg"
alt="Polars and Narwhals: Understanding Expressions When You're Used to pandas" width="50%" /></a>

## Transcript
