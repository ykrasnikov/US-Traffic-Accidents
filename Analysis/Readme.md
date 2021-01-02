# Team 3 Project Analysis: Traffic Accidents

## Content:
### 1. Data Set Analysis And Clean-up
### 2. Accidents by States 
### 3. Accidents by TX Counties
### 4. Weather Conditions effect accidents 
### 5. Road Amenity effect
### 6. Daytime effect
### 7. Day of Week effect 
### 8. Holidays effect 
________________________


# 1. Data Set Analysis And Clean Up 

## 1.1 Original Data Set 

## US Traffic Accidents
https://www.kaggle.com/sobhanmoosavi/us-accidents?select=US_Accidents_June20.csv

 Countrywide car accident dataset, which covers 49 states of the USA. The accident data are collected from February 2016 to June 2020, using two APIs that provide streaming traffic incident (or event) data. These APIs broadcast traffic data captured by a variety of entities, such as the US and state departments of transportation, law enforcement agencies, traffic cameras, and traffic sensors within the road-networks.


### 2016 and 2020 is not full so dataset was filtered for 2017,2018,2019

## US population 
https://www.census.gov/data/tables/time-series/demo/popest/2010s-total-cities-and-towns.html

___________________
## 1.2 Data Overview : Null Values
_________________________
Data field| Count
---|---
ID |                      2563837
Source|                   2563837
TMC|                      1965015
Severity|                 2563837
Start_Time |              2563837
End_Time |                2563837
Start_Lat  |              2563837
Start_Lng   |             2563837
End_Lat      |             598822
End_Lng     |              598822
Distance(mi)  |           2563837
Description  |            2563836
Number      |              928610
Street     |              2563837
Side       |              2563837
City       |              2563781
County     |              2563837
State      |              2563837
Zipcode    |              2563073
Country    |              2563837
Timezone   |              2560804
Airport_Code  |           2558452
Weather_Timestamp |       2530471
Temperature(F)  |         2514321
Wind_Chill(F) |           1080688
Humidity(%)   |           2511771
Pressure(in)  |           2520881
Visibility(mi)  |         2507022
Wind_Direction   |        2522105
Wind_Speed(mph) |         2200487
Precipitation(in)  |       938871
Weather_Condition |       2506557
Amenity       |           2563837
Bump     |                2563837
Crossing   |              2563837
Give_Way    |             2563837
Junction  |               2563837
No_Exit      |            2563837
Railway      |            2563837
Roundabout   |            2563837
Station      |            2563837
Stop       |              2563837
Traffic_Calming  |        2563837
Traffic_Signal  |         2563837
Turning_Loop   |          2563837
Sunrise_Sunset  |         2563778
Civil_Twilight  |         2563778
Nautical_Twilight  |      2563778
Astronomical_Twilight  |  2563778
Year                |     2563837
______________________
### Observations:
Good qaulity data set - minimal null values , for our area of analysis data set is quite full :
________________________
Data field| Count
---|---
ID |                      2563837
Source|                   2563837
Severity|                 2563837
Start_Time |              2563837
End_Time |                2563837
Start_Lat  |              2563837
Start_Lng   |             2563837
Description  |            2563836
Street     |              2563837
Side       |              2563837
City       |              2563781
County     |              2563837
State      |              2563837
Zipcode    |              2563073
Country    |              2563837
Temperature(F)  |         2514321
Wind_Chill(F) |           1080688
Humidity(%)   |           2511771
Pressure(in)  |           2520881
Visibility(mi)  |         2507022
Wind_Speed(mph) |         2200487
Precipitation(in)  |       938871
Weather_Condition |       2506557
Amenity       |           2563837
Astronomical_Twilight  |  2563778
Year                |     2563837
___________________

## 1.3 Data Source 

<img src="output/YK_US_accidents_source_bar.png" align="left" width="400"/>
<img src="output/YK_TX_accidents_source_bar.png" align="center" width="400"/>

### Observations:

75% of Data is coming from MapQuest Traffic API , 24% from Bing Maps Traffic API and 1% hybrid

**_LINK TO CODE - [YK_US_Data_traffic_analysis.ipynb](../CODE_data_cleanup/YK_US_Data_traffic_analysis.ipynb)_**

**_LINK TO CODE - [YK_TX_Data_traffic_analysis.ipynb](../CODE_data_cleanup/YK_TX_Data_traffic_analysis.ipynb)_**

## 1.4 Data Overview by State
#### Data distribution by State and by year
<img src="output/YK_US_accidents_States_bar.png" align="center" width="600"/>

### Observations:

**_LINK TO CODE - [YK_US_Data_traffic_analysis.ipynb](../CODE_data_cleanup/YK_US_Data_traffic_analysis.ipynb)_**


_______________________

## 1.5 US States census data 2019 
<img src="output/YK_US_States_Census_bar_plt.png" align="center" width="600"/>

### Observations:

**_LINK TO CODE - [YK_clean_census_data_USstate_TXcounty.ipynb](../CODE_data_cleanup/YK_clean_census_data_USstate_TXcounty.ipynb)_**

______________________


## 1.6 Accidents by month-year 
#### US Accidents Bar Chart
<img src="output/YK_US_accidents_yearmonth_bar.png" align="center" width="600"/>

#### TX Accidents Bar Chart

<img src="output/YK_TX_accidents_monthYear_bar.png" align="center" width="600"/>


### Observations:
You can observe jump in accidents count on US bar chart  from Jul 2017 to Aug 2018 , in H1 2017 data was averaging around 45K and rest of the data is averaging around 70+K. We attribute this to qaulity of data set, and if season related analysis needs to be done data for 2017 have to be excluded. 
Texas sample for 2017 does not contain any significant variations - so for TX all  3 years can be used

**_LINK TO CODE - [YK_US_Data_traffic_analysis.ipynb](../CODE_data_cleanup/YK_US_Data_traffic_analysis.ipynb)_**

**_LINK TO CODE - [YK_TX_Data_traffic_analysis.ipynb](../CODE_data_cleanup/YK_TX_Data_traffic_analysis.ipynb)_**
_____________________

# 2 Accidents by States Analysis

## 2.1 Accidents by States
#### GMAP US States Accidents Rates per 1000 People , color scale from low - light yellow to high - purple. 
<img src="output/US States AAR Map.png" align="center" width="600"/>

### Observations:
South Carolina stands out with higher rate.
#### Scatter plot  US States Accidents  

<img src="output/YK_US_accidents_scatter_plt.png" align="center" width="600"/>
<img src="population_density.png" align="right" width="200"/>


### Observations:
In general – densely populated areas - California, Florida, East and North East States are corresponded to higher traffic accidents frequency.

**_LINK TO CODE - [YK_chart_State_AAR.ipynb](../CODE_analysis/YK_chart_State_AAR.ipynb)_**

**_LINK TO CODE - [YK_accident_scatter_plot.ipynb](../CODE_analysis/YK_accident_scatter_plot.ipynb)_**

**_LINK TO CODE - [YK_State_AAR.ipynb](../CODE_analysis/YK_State_AAR.ipynb)_**

____________________

## 2.2 Top 10 States by Total Yearly accidents and top accident rate per 1000 people (averaged over 3 years)
<img src="output/YK_US_States_Accidents_bar_plt.png" align="left" width="400"/>
<img src="output/YK_US_States_AARs_bar_plt.png" align="center" width="400"/>

### Observations:
Accordingly to TX DOT , 562K crashes were reported in 2019. Our data set has 82K , which is a good size sample.

**_LINK TO CODE - [YK_States_TXCounties_barcharts.ipynb](../CODE_analysis/YK_States_TXCounties_barcharts.ipynb)_**

**_LINK TO CODE - [YK_State_AAR.ipynb](../CODE_analysis/YK_State_AAR.ipynb)_**

_______________

# 3 Accidents by TX County Analysis
## 3.1 Accidents by States
#### GMAP TX Counties Accidents Rates per 1000 People , color scale from low - light yellow to high - purple. 
<img src="output/TX_Counties_AAR_Map.png" align="center" width="600"/>

### Observations:
Travis county with Austin stands out with a higher rate.
#### Scatter plot  TX Counties Accidents  

<img src="output/TX_US_accidents_scatter_plt.png" align="center" width="600"/>



### Observations:
In general – densely populated areas - Harris(Houston), Dallas, Travis (Ausitn), Bexar(San Antonio) megapoloices  are corresponded to higher traffic accidents frequency.
___________________
County|	Yearly Accident rate | Population
---|---|---
Harris|	27582.0|4,646,630
Dallas|	18139.3|2,606,868
Travis|	17343.3|1,226,805
Bexar	|6449.0|1,952,843
Tarrant	|4370.7|2,049,770
El Paso	|3162.3|836,062
_____________	

**_LINK TO CODE - [YK_chart_County_AAR.ipynb](../CODE_analysis/YK_chart_County_AAR.ipynb)_**

**_LINK TO CODE - [YK_accident_scatter_plot_TX.ipynb](../CODE_analysis/YK_accident_scatter_plot_TX.ipynb)_**

**_LINK TO CODE - [YK_TXcounty_AAR.ipynb](../CODE_analysis/YK_TXcounty_AAR.ipynb)_**

____________________

## 3.2 TX Counties : Top 10 accident rate per 1000 people (averaged over 3 years)

<img src="output/YK_TX_Counties_AARs_bar_plt.png" align="center" width="400"/>

### Observations:
Travis county stands out .

**_LINK TO CODE - [YK_States_TXCounties_barcharts.ipynb](../CODE_analysis/YK_States_TXCounties_barcharts.ipynb)_**

**_LINK TO CODE - [YK_TXcounty_AAR.ipynb](../CODE_analysis/YK_TXcounty_AAR.ipynb)_**

_______________
# 4 Texas Weather and Traffic Effects

From 2017 to 2019, there were 248,299 traffic incidents on Texas roads. What role did weather play in those incidents?
_________________
## 4.1 Seasons effect
Do the 4 seasons matter in Texas in relation to accidents/incidents?
### Observations:
There is no significant difference in the number of incidents in Texas between each of the seasons. Fall is slightly higher than the rest of the seasons.

<img src="output/TAbyseason.png" align="center" width="400"/>

### Observations:
Fall is slightly elevated with 64,670 incidents, Winter has 63,184, Spring has 61,900 and Summer has the least with 58,544.
___________________

## 4.2 Weather Conditions
In what type of weather conditions do we find the most incidents in Texas?

<img src="output/WeatherConditions.png" align="center" width="400"/>

### Observations:
Strangely enough, when it comes to Texas Highways, Clear weather has the most incidents with around 60,000 during the 3 year period.   This 20,000 more
than the next highest cause - Mostly Cloudy.   Cloudiness seems to be a slight factor in the majority of all other incidents.  Any type of cloudiness, seems to 
affect the overall ability to drive in Texas.  It was expected that a heavy rain would be more of a cause of concern but that was not the case.  Light rain caused
more of an issue than the heavier rain.   Ice/Snow were really not a factor due to limited occurrences in the State of Texas. 
_____________________
## 4.3 Time of the day effect
In the top 10 weather conditions, is time of day a factor?

<img src="output/TODWeatherConditions.png" align="center" width="400"/>

### Observations:
As we can see from the chart, more accidents happen during the day than they do at night.  Overcast skies had a larger role at night than all other weather conditions
with the exception of clear. 
___________________________
## 4.4 Accident Severity vs Weather effects
What type of delays are caused by these incidents?

<img src="output/SeverityWeatherConditions.png" align="center" width="400"/>

### Observations:
Severity shows the severity of the accident in terms of traffic impact. One being the least, four being the most. In the top 10 weather conditions, the majority of the accidents fall into the 2 and 3 severity levels. For the most part, they fall into category 2 meaning that there is a slight delay when an accident occurs.
_____________________
##  4.5 Visibility effect
Does visibility play a factor in traffic incidents in Texas?

<img src="output/visability.png" align="center" width="400"/>

### Observations:
No, there was no correlation that limited visibility caused any additional effects on whether an incident occurred or not.  The majority of the incidents reported had a 10 mile
visibility supporting this conclusion.  While this data covered traffic delays it did not dive into the true causes of these incidents, one site on the internet gave the top 5 reasons
for accidents in Texas were failure to control speed, driver inattention, failure to drive in a single lane, failure to yield when turning left and usafe lane changes.  Tailgatig was a close sixth cause.  

**_LINK TO CODE - [pb_WeatherEffects-Final.ipynb](../CODE_data_cleanup/pb_WeatherEffects-Final.ipynb)_**
___________________
# 5. Road Amenity effect
 
**Evaluating Car Accidents in Texas by Traffic Safety Amenities and Time of Day**

## 5.1 Traffic Safety Amenities
### Observations:
Of the auto accidents recorded in Texas from years 2017-2019, only about half recorded traffic safety amenities involved in the accidents. The overwhelming plurality of these accidents involved traffic_signals. Second and thrid runners-up are awarded to Junctions and Crossings.

<img src="output/accidents_per_amenity.png" align="center" width="400"/>

### Observations:
Based on this evidence, we assume intersections for automobils and pedestrians alike are the settings for higher accident rates.
_______________________________
# 6. Time of Day Effect

More accidents happen during the daytime vs. the nightime by about 4/1. 

<img src="output/day_night_accident_share.png" align="center" width="400"/>

Given this distribution, we broke the date down a little more:

<img src="output/accidents_per_hour.png" align="center" width="400"/>

### Observations:
Obviously, there is a greater distribution of accidents by daytime hours than night time. Even further, there seem to be spikes in accident traffic during the hours of 6:00am to around 11:00am and then again from 4:00pm to 7:00pm: representing some really-bad-mronings and evenings for rush hour commuters.

**_LINK TO CODE - [cars_vs_ammenities_texas](../amenities-and-time-of-day/cars_vs_ammenities_texas.ipynb)_**

# 7. Day of the week/month effect
## 7.1 Month effect

<img src="output/OO_TX_accidents_month_barplot.png" align="center" width="600"/>

### Observations:

We analyzed the data to see if we can find how the traffic delays related to accidents vary throughout the months, day of the week and propose some explanations for the observed distributions
The graph below shows the variations of traffic delays with the month. We see that the number of traffic delays is progressively lower as we go into the summer months with the lowest number of traffic delays due to accidents on the month of July. The number of delays goes back to high numbers in August, which we interpret as "return to work/classes effect"  
__________________
## 7.2 Weekdays effect
<img src="output/OO_TX_accidents_dayofweek_barplot.png" align="center" width="600"/>


### Observations:
The next analysis done with this data (from Texas) was to prove if Fridays are the day of the week when most traffic delays occur. Our intuition and common sensense suggests that on Fridays people are getting paid, want to go back home fast or have some alcohol to celebrate, hence there are more chances for accidents and traffic delays. However, the analysis of the data shows that Friday is not very different in the number of traffic slow-downs due to accidents than other days of the standard work week. However, on weekends (Saturday and Sunday) slow-downs due to accidents are less frequent. One interpretation is that less people are driving and hence traffic is smoother on weekends. Curiously, on Mondays traffic slow-downs due to accidents is lower than any other day of the work week and perhaps this is due to higher degree of awareness and less fatigue at the start of the work week.
___________________________
<img src="output/OO_TX_accidents_dayofweekre-scaled_barplot.png" align="center" width="600"/>

### Observations:
In order to see better the details of the differences in the day of the week effect we re-scaled the y axis, as shown below. When we use a different scale in the y axis the difference in number of slow-downs for the weekdays is clearer. Surprisingly, Tuesdays have the highest number of traffic slow downs, but the reasons are not well-understood. Friday comes second in the ranking and this could indicate that our hypothesis is at least partially correct.
________________
## 7.2 Day of month effect
<img src="output/OO_TX_accidents_dayofmonth_barplot.png" align="center" width="600"/>

### Observations:
Finally, we analyzed the distribution of traffic delays per day of the month in Texas. The variability is not easy to understand. The graph below suggests that most days of the calendar month have similar number of slow-downs due to accidents. Four months of the year have 30 days and seven months have 31 days, February has either 28 or 29 days. It is not very clear that the end of the month, a common payday, has a strong effect on the number of slow-downs due to accidents. The average of slow-downs due to accidents is not greater on a 30th day than any other day of the month, although the average number of slow-downs on the 31st could be (comparatively) greater than any other day of the month if we double the count observed.
_________________________
Below we give a link to the code that contains the portions of the project related to the table of content #7. This part of the code also contains the reading of the csv file, the conversion of strings to datetime timestamps and the creation of a dataframe with extra columns for each part of the timestamp (year, month, day, hour, minute, second) of the start and end of the traffic slow downs. The timestamps have to be separated to do arithmetic operations and analyses of the distribution of slow downs due to accidents. The month of the year was used to identify in which season a delay in traffic due to an accident occurred, in adddition to other analyses that have been used throughout the project. We used the csv output of the dataframe to share the timestamp fractionation.
**_LINK TO CODE - [orlando_code](../ooCode/oo01022021.ipynb)_**

# 8. Holidays Effect
in order to remove day of the week variation we will anylize distribution by week day ,US data sample ( 2018-2019).

<img src="output/YK_US_accidents_weekday_boxplot.png" align="center" width="400"/>

_______________
 data  |Mon|Tue|Wed|Thu|Fri|Sat|Sun
---|---|---|---|---|---|---|---
mean|3025|	3201|	3170|	3055|	3188|	1090|	962
median|	2941|	3115|	3110|	3080|	3102|	982|	887|
________________________
### Method:
Next we merge lower quartile data with holidays dates 
_______________________

Date|US Holiday|Accidents Count lower quartile|Year|Month
---|---|---|---|---
2018-01-01|New Year's Day|980.0|2018.0|1.0
2018-01-15|Martin Luther King Jr. Day|||
2018-05-28|Memorial Day|1860.0|2018.0|5.0
2018-07-04|Independence Day|1593.0|2018.0|7.0
2018-09-03|Labor Day|1644.0|2018.0|9.0
2018-11-12|Veterans Day|||
2018-11-22|Thanksgiving|2051.0|2018.0|11.0
2018-12-25|Christmas Day|682.0|2018.0|12.0
2019-01-01|New Year's Day|1177.0|2019.0|1.0
2019-01-21|Martin Luther King Jr. Day|2483.0|2019.0|1.0
2019-05-27|Memorial Day|1734.0|2019.0|5.0
2019-07-04|Independence Day|1350.0|2019.0|7.0
2019-09-02|Labor Day|2250.0|2019.0|9.0
2019-11-11|Veterans Day|||
2019-11-28|Thanksgiving|985.0|2019.0|11.0
2019-12-25|Christmas Day|1278.0|2019.0|12.0

### Observations:
All US holidays with exception of Veteran Day & Martin Luther King Day are within lower quartiles , indicating lower traffic accident rates


**_LINK TO CODE - [YK_US_Data_traffic_analysis](../CODE_data_cleanup/YK_US_Data_traffic_analysis.ipynb)_**