# Team 3 Project Analysis: Traffic Accidents

## Content:
### 1. Data Set Analysis And Clean-up
### 2. Accidents by States 
### 3. Accidents by TX Counties
### 4. Weather Conditions effect accidents 
### 5. Daytime effect
### 6. Road Amenity effect
### 7. Payday effect 
### 8. Holidays effect 


## 1. Data Set Analysis And Clean Up 

## 1.1 Original Data Set 

## US Traffic Accidents
https://www.kaggle.com/sobhanmoosavi/us-accidents?select=US_Accidents_June20.csv

 Countrywide car accident dataset, which covers 49 states of the USA. The accident data are collected from February 2016 to June 2020, using two APIs that provide streaming traffic incident (or event) data. These APIs broadcast traffic data captured by a variety of entities, such as the US and state departments of transportation, law enforcement agencies, traffic cameras, and traffic sensors within the road-networks.


### 2016 and 2020 is not full so dataset was filtered for 2017,2018,2019

## US Cities population 
https://www.census.gov/data/tables/time-series/demo/popest/2010s-total-cities-and-towns.html


## 1.2 Data Overview : Null Values

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

### Observations:
Good qaulity data set - minmal null values , for our area analysis data set is full

## 1.2 Data Overview : Data Source 

<img src="output/YK_US_accidents_source_bar.png" align="center" width="400"/>

### Observations:

Data is mainly coming from mapQuest ......blablala
blala vlvl
vlvlv
bllbb

**_LINK TO CODE - [YK_Data_traffic_analysis.ipynb](CODE_data_cleanup/YK_Data_traffic_analysis.ipynb)_**

## 1.3 Data Overview : Cloudiness & Wind Speed vs Latitude

<img src="Images/cloud_lat.png" align="left" width="200"/>
<img src="Images/wind_lat.png" align="center" width="200"/>

Observations:

scatter of cloudiness vs latitude - we can observe some grouping around 0, 20, 40, 75, 90, 100% lines ... this could be due to the way cloudiness is measured/evaluated.
scatter of wind speed vs latitude - we can observe some grouping below 10 mph

