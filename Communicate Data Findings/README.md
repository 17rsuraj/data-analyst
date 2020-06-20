# Project : Communicate Data Findings
#### Submitted By: Suraj Gurav

## Dataset

_Ford GoBike System Data_ is used for this project.
The data files are obtained from the [Source](https://s3.amazonaws.com/baywheels-data/index.html)
Here the monthwise data is available starting from January 2018 to May 2020. However, everything is updated on 10th Jan 2020. Going through some of the _.csv_ files manually, I found that most of the data is missing from some files.

Hence, the selected data for this project is only **from January 2018 to March 2018**

## Data Wrangling

Data wrangling is done in 3 steps such that - 
1. Data Gathering : Download the _.zip_ files from above mentioned source and extract the _.csv_ files from it
2. Data Assessment : Performing visual as well as programatic assessment to identify quality and tidiness issues
3. Data Cleaning : Solving all quality related issues to get the cleaned dataset to perform analysis

After cleaning the dataset, few more columns are added, which are useful for the further data exploration. Finally, this final dataset is saved as `ford_gobike_data_extended.csv`.
Also, for using the dataset for explanatory data analysis and visualizations a pickle file `ford_gobike_data_extended.pkl` is also generated.

## Exploratory Data Analysis

Exploratory Data Analysis is perfomed with the help of K-Means clustering, univariate, bivariate and multivariate data analysis.

In the data wrangling step, some clusters were identified in the dataset. These clusters were made up of Ford GoBike _start_station_id_ and _end_station_id_. To visualize these clusters and their location co-ordinates, K-Means clustering is used. Through K-means clustering, labels for the data are generated. Then, to visualize these clusters on the actual map, `folium` package is used. Together with the visualization of K-Means clustering and Folium map, 3 location clusters were identified and labeled as **San Francisco, East Bay** and **San Jose**.

With the help of univariate exploration, individual variables such as frequent start and end stations, genders of the GoBike users, type of users such as subscribers and customers, age of the GoBike users are explored.

The bivariate explorations are used to unlock the relationships between two variables. In this section, most frequent GoBike trip routes, distribution of trip duration over user age and over weekdays is explored.

Multivariate explorations are used to identify trends and patterns in the data, when more than 2 variables are analysed simultaneously.

## Summary of Findings

_**The findings from the univariate exploration**_ - 

* San Francisco Caltrain (Townsend St at 4th St) is the most frequent start and end station. It is used as end station more number of times than as start station.

* 08:00 O'clock in the morning and 05:00 O'clock in the evening is found to be busiest time in a day. 

* As compared to female members, more number of male members used Ford GoBike system. Also, there are more number of subscribers than the customers. 

* Looking at the location clusters, _San Francisco_ seems to be popular among all, such that, 75% of people start their journey at _San Francisco_. 

* 72 % of Ford GoBike system users are people younger than 40 years age. Maximum number of people are of 30 years. 

_**The findings from the bivariate exploration**_ - 

* The route connecting _San Francisco Ferry Building (Harry Bridges Plaza)_ to _The Embarcadero at Sansome St_ is the most frequently used route

* The average GoBike trip duration on weekends is higher than that of on weekdays. 

* The average GoBike trip duration decreases with increase in the age of the user. This trend continues till the age group (30,40]. Beyond this stage, the average trip duration starts increasing again.

_**The findings from the multivariate exploration**_ - 

* No any relationship among _dayofweek, duration_sec_ and _age_ variables is observed.

* Most of trips start and end within the same hour resulting in average trip duration less than 1 hour. 

## Key Insights for the Presentation

For the presentation, I selected the the visualizations focusing on distribution of the Ford GoBike users, trip routes, and distribution of GoBike trip durations.

Below are the key insights which I presented in the presentation slide deck.

1. Busiest time of day

08:00 O'clock in the morning and 05:00 O'clock in the evening is found to be busiest time in a day. Moderate number of trips were recorded between 08:00 am and 05:00 pm, however, low number of trips occured beyond this time window. The trend is similar during all the first 3 months of 2018.

2. Age wise distribution of Ford GoBike users

All the users of GoBike of age younger than 60 years are divided in 5 groups with the range of 10 years. 39% of the members are observed in age group of 30 to 40 years and 33% member belong to age group of 20 to 30 years of age

3. Most frequent trip routes

A route is defined as combination of a start station to a end station. The route connecting _San Francisco Ferry Building (Harry Bridges Plaza)_ to _The Embarcadero at Sansome St_ is the most frequently used route.

4. Trip duration distribution over the week

Low average trip duration is observed on weekends, however it is highest on the weekends.

5. Trip duration distribution over age of the user

The average trip duration shows decreasing trend with increase in the age of the user. However, this trend is reversed beyond 40 years of age.

6. Trip duration distribution over start and end time in a day

Trips usually start and end in the same hour. The average trip duration approximately 12 minutes for entire dataset, backs up this finding.






