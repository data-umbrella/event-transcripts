# Analyzing Geospatial Forest Data with Geopandas and Rasterio (Laya Zeinali Yadegari)

## Alternate Titles
- Analyzing Geospatial Forest Data with Geopandas and Rasterio

## Upcoming Events
Join our Meetup group for more events!
https://www.meetup.com/data-umbrella

## Key Links
- video: https://youtu.be/QW4XsceFxv4


## Resources
- slides: https://github.com/data-umbrella/event-transcripts/blob/main/resources/geospatial_laya_zeinali.pdf

## About the Event
In this session, we will explore how to model forest structure and quantify ecosystem services using Python and Earth observation data. Leveraging GEDI, Sentinel-1, Sentinel-2, and SRTM datasets, we’ll walk through data preprocessing, machine learning techniques (e.g., Random Forest), and interpretation using SHAP for understanding feature importance.

- Overview of forest structure, aboveground biomass (AGB), and ecosystem service indicators
- Preprocessing spatial and tabular data using Python (geopandas, rasterio, pandas)
- Machine learning approaches for forest modeling: Random Forest, feature selection, and model evaluation

## Timestamps
```
00:00 Data Umbrella introduction 
04:48 Laya begins presentation
05:30 Introduction to research background (forest ecosystem, technical approach, remote sensing, environmental impact)
06:35 Geospatial forest analysis introduction
08:15 Forest biomass and carbon
09:04 Hyrcanian forest study area overview
10:56 Six (6) data sources (icons included)
12:09 An integrated approach to modeling forest canopy height and aboveground biomass using GEDI, Sentinel-1, Sentinel-2, SRTM, and LULC data
13:20 Why Python for geospatial analysis? 
15:53 Step 1: Setting up libraries on Google Colab notebook (11 used) + some background
18:50 Resolving technical issues
21:04 Step 2: Continued setup (loading image properties, loading datasets)
22:26 Step 3: Preparing dataset for machine learning
23:56 Step 4: Performing exploratory data analysis (EDA)
24:15 Step 5: Creating box and density plot for canopy height
25:07 Step 6: Creating a bar plot to show mean spectral reflectance for each band (Sentinel-2 example)
25:48 Step 7: Creating a box plot to visualize the distribution and potential outliers for each feature with some measures of central tendency
26:34 Step 8: Creating a kernel density plot to visualize the distribution of each feature and target variable
27:07 Step 9: Addressing low variance and outliers
27:53 Step 10: Training a model (random forest regression example)
29:36 Step 11: Plotting a graph to show the performance of the model
30:23 Step 12: Producing the canopy height map (CHM)
31:06 Performing explainable machine learning (xML) using SHAP (SHapley Additive exPlanations), Universal Transverse Mercator (UTM) coordinates, Google Earth Engine (GEE), and more
43:22 Working with GEDI (Global Ecosystem Dynamic Investigation) data
50:24 Random forest algorithm results
51:30 Feature importance
53:38 Diagnosis with matplotlib and seaborn libraries, Hyracanian forest characterization
56:50 Results presentation
58:42 Advances in Space Research Journal study (Title: Mapping above-ground biomass in old-growth deciduous forests using open-access satellite data, field plots, and machine learning algorithms)
1:00:11 Q&A

```


## About the Speaker
As a Ph.D. candidate at Tarbiat Modares University, Tehran, Laya's research interests lie in forest remote sensing and the assessment of forest ecosystem services. She is currently investigating the application of machine learning techniques to analyze multi-sensor remote sensing data, including LiDAR, radar, and optical imagery, for the estimation of forest carbon stocks, biomass, and the provision of ecosystem services. Her research specifically utilizes GEDI (Global Ecosystem Dynamics Investigation)

- LinkedIn: https://www.linkedin.com/in/laya-zeinali-2667171ba/
- GitHub: https://github.com/layazeinali

#Python #forestmodeling #MachineLearning

 
## Video 
<a href="http://www.youtube.com/watch?feature=player_embedded&v=QW4XsceFxv4" target="_blank"><img src="http://img.youtube.com/vi/QW4XsceFxv4/0.jpg" alt="Analyzing Geospatial Forest Data with Geopandas and Rasterio" width="50%" /></a>

## Transcript
