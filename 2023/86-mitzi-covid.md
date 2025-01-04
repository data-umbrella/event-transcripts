# Mitzi Morris:  Lessons from COVID-19: Non-random Missing Data and Its Consequences

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- Transcript: https://github.com/data-umbrella/event-transcripts/blob/main/2023/86-mitzi-Covid.md
- Meetup Event: https://www.meetup.com/data-umbrella/events/294762228/
- Video:  https://youtu.be/Rj33tjUomSU
- GitHub repo:  
- Transcriber:  ? [needs a transcriber]

## Resources
https://github.com/rtrangucci/epi-missing-data
- Slides: https://github.com/mitzimorris/epistan_talk_2023_08_08/blob/main/slides.pdf
- JSM presentation:  Unifying Design-Based and Model-Based Sampling Inference, https://statmodeling.stat.columbia.edu/2023/08/06/unifying-design-based-and-model-based-sampling-inference-my-talk-at-the-joint-statistical-meetings-in-toronto/

## About the Event
A fundamental challenge for survey and observational datasets is that not all records in the dataset are complete; key pieces of information may be missing.

In this talk I work through the models and methods from the paper
MODELING RACIAL/ETHNIC DIFFERENCES IN COVID-19 INCIDENCE WITH COVARIATES SUBJECT TO NON-RANDOM MISSINGNESS

They write:
In emergency situations, such as a surging pandemic, it is easy to see how the disease process itself may induce non-random missingness of covariates. For example, during a period of rapidly increasing caseloads, such as the Delta and Omicron surges of the COVID-19 pandemic, the overwhelming number of cases is likely to limit the ability of case investigators to collect data that are as detailed as those collected during lower-incidence periods. These differences may also be more pronounced when comparing wealthier and poorer jurisdictions with differential resources for case-finding and intervention.
Using the Stan language and CmdStanR interface, together with a simulated dataset of Covid-19 cases and population demographics, where age, gender, race/ethnicity, and neighborhood have varying degrees of missingness, we will demonstrate how different approaches produce different estimates of Covid-19 prevalence among key demographics.

```
## Timestamps
00:00 Beryl introduces R-Ladies
00:24 R-Ladies Overview begins (Agenda)
00:42 What is R-Ladies?
01:24 R-Ladies global chapter map
02:00 R-Ladies NYC
03:03 Getting involved with R-Ladies NYC, contact info
04:02 Data Umbrella introduction
08:45 Speaker introduction
09:45 Mitzi begins talk
11:24 Outline / agenda - paper discussion (Trangucci et al)
12:50 COVID-19 in Michigan
15:56 Michigan mortality rates March-October 2020 w/ disparities
17:21 What’s the infection rate? 
19:00 Discussing data missingness relating to demand for public health resources, under-resourced populations
20:27 Missing data types (MCAR, MAR, NMAR)
23:24 Survey data vocabulary / terminology (e.g. strata)
26:24 Simulation Study Data + description of strata variables
28:08 2010 Census Data for Wayne County, MI
29:18 Simulated Dataset example
31:14 Simulation Study Models (multiple imputation breakdown)
33:30 Fig 1 - Model Bias for Disease Prevalence
36:45 Fig 2 - Model Bias for Relative Risk
38:52 Modeling Disease Prevalence
40:44 Modeling Missingness
45:00 Missingness independent of strata and justifying the Bayesian joint hierarchical model
46:38 Priors for Model
47:47 Priors for Likelihood; missingness varies by race and age-sex strata
49:50 Theorem and Priors for Model 2.2 (conditions for the data)
52:40 Model 2.3 - Adding geo-location
52:49 Conclusion and thanks
55:36 References; Q&A begins
56:54 Q&A - How often does missing data go unaddressed?
59:28 Q&A - Sampling weights or post-stratification
1:02:45 Q&A - Request and context around longer tutorial, closing words
```
https://github.com/data-umbrella/event-transcripts/issues/92

## About the Speaker
Mitzi Morris
- GitHub:  https://github.com/mitzimorris

#python #statistics #machinelearning 

## Video
<a href="http://www.youtube.com/watch?feature=player_embedded&v=Rj33tjUomSU" target="_blank"><img src="http://img.youtube.com/vi/Rj33tjUomSU/0.jpg"
alt="Lessons from COVID-19: Non-random Missing Data and Its Consequences" width="50%" /></a>

## Transcript
