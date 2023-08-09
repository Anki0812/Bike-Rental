# Bike Rental
> A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
#### Background of the Project:
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 

#### Business Problem:
BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


#### Dataset Used:
We are using 'Day Dataset' it contains the complete bike retal data for all bike rented through the time period 2018 to 2019.
The dataset used in this project contains information about bike rental count against different parameters like weather, holiday, humidity, windspeed etc.

Below is the data dictionary related to data set
- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	- weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

## Conclusions

- The rental count in 2019 is around 20% more than in 2018.
- Bikes are rented mostly on non holiday (around 97%).
- The rental count during weekdays is almost the same. 
- Around 70% bikes are rented on a clear day and least on snowy or rainy day
- Maximum number of bikes are rented in Fall, followed by Summer, Winter, Spring.

- Variables significant for predicting demand
    - Year
    - Season - Fall being most ideal
    - Windspeed
    - Working day
    - Weather - Clear day being more ideal

- Listed below 4 Models
    - Model 1 
        - Variables - year_2019, windspeed, season (fall, winter, summer), months (march, august, september, october), weather(rainy, cloudy), weekday(saturday), holiday
        - Train r2 score(Adj) - 0.782
        - Test r2 score - 0.750
    - Model 2 
        - Variables - year_2019, windspeed, months (february, march, april, may, june, july, august, september, october, november, december), weather(rainy, cloudy), weekdays (wednesday, friday, saturday), holiday
        - Train r2 score(Adj) - 0.797
        - Test r2 score - 0.742
    - Model 3 
        - Variables - year_2019, windspeed, season (winter, summer), months (march, august, september, october), weather(rainy), humidity
        - Train r2 score(Adj) - 0.813
        - Test r2 score - 0.780
    - Model 4 
        - Variables - year_2019, windspeed, season (winter, summer), months (march, august, september, october), weather(rainy)
        - Train r2 score(Adj) - 0.805
        - Test r2 score - 0.736

## Technologies Used
- numpy - version 1.21.3
- pandas - version 1.5.3
- matplotlib - version 3.4.3
- seaborn - version 0.12.2
- sklearn - version 1.2.1
- statsmodels - version 0.13.5

## Acknowledgements
- The training provided by IIIT Bangalore greatly contributed to the successful execution of this project.
- This project was based on [this tutorial](https://learn.upgrad.com/course/4617/segment/27465/225458/689472/3488520).


## Contact
Created by [@Anki0812] - feel free to contact.


