## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

Ryan Kruse:  Building a Political Census with Placekey

## Key Links
- Transcript:  https://github.com/data-umbrella/event-transcripts/blob/main/2021/23-ryan-placekey.md
- Meetup Event:  https://www.meetup.com/data-umbrella/events/276090431/
- Video:   https://youtu.be/NYV4fB3IU0k
- Colab Notebook: https://colab.research.google.com/drive/1i3yzeWNsJ5huwX7-frEgwz_Sb_CZEFyh?usp=sharing  

## Resources (from chat)
- Link to Placekey community - https://www.placekey.io/community
- Mapping H3 to real world: https://placekey.github.io/placekey-notebooks/advanced_functionality.html

```text
## Agenda
00:00 Reshama introduces Data Umbrella
06:15 Ryan begins presentation 
07:09 Objectives (power of geospatial data)
07:44 Introduction: Political Affiliation Census
09:43 What datasets do we need?
12:06 Intro to Placekey
15:40 Methods (read in data, joining, normalizing)
17:00 Google Colab notebook, with example
18:42 read in data
31:45 normalize data
34:59 map of Minnesota
35:45 back to slides: limits and considerations
35:55 Ethics & privacy
36:32 Sampling bias
37:23 Adjusting for mail-in ballots
38:14 Missing estimates (imputation options)
39:02 Conclusion
40:38 Q: CBG is census block group. What is POI?
40:54 Q: What are other applications of Placekey?
42:07 Q: Is Placekey fairly new? What was used before?
43:25 Q: Can you use Placekey for COVID data?
44:35 Q: How about international data? Does Placekey work for that?
45:43 Q: Presentation used Colab and Python. Can other programming languages or software be used?
47:35 Q: How do you choose which country data will be added to the API?
48:53 Q: How many digits is the Placekey code?
49:30 Q: Do locations that are water have a Placekey?
50:24 Q: Is the Placekey code connected to LAT and LONG?
52:30 Closing words by Ryan
```

## Outline
- Objectives
- Introduction
- Assumptions
- Methods
- Live code demo
- Limitations & Considerations
- Conclusion

## Event
This webinar will introduce you to Placekey, a handy tool for joining geospatial data, applied to building a "political census." Political affiliation data is typically only available at the county or district level, but Placekey allows us to join foot traffic data (from SafeGraph) with Election Day voter results to estimate political affiliation at much higher resolution. We'll talk about some of the limitations of our analysis, and we'll also briefly survey the value Placekey brings over some of the other tools out there.

## About Placekey
What is Placekey? Placekey is a free, universal standard identifier for any physical place, so that the data pertaining to those places can be shared across organizations easily.

However, Placekey goes beyond just an identifier. It’s a movement of organizations and individuals that prize access to data. Placekey members want geospatial data that is easily joined and combined...because real answers come from combining data from many different sources. It is a philosophy that data should be easy to access, and data should not be hoarded. These members believe that data, when combined, can do massive good.

## Speaker
I completed my Master's in Data Science at Minnesota State University-Mankato in December 2020. I work as a Data Science Consultant/Community Manager for SafeGraph. I enjoy using data in creative ways to solve problems.

- GitHub: https://github.com/kruser1
- LinkedIn: https://www.linkedin.com/in/ryan-kruse-19619311b/
- Twitter: https://twitter.com/RyanThomasKruse

