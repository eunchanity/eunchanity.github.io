---
layout: post
title: Project 1 - Exploratory Data Analysis
---

### Prompt:
```
---
A potential client, WomenTechWomenYes(WTWY), has an annual gala at 
the beginning of the summer and wants to utilize the power of data 
and analytics to optimize the effectiveness of their street team 
work. The client is seeking to fill the event space with people 
passionate about increasing the participation of women in technology,
and to concurrently build awareness and reach. To this end, 
they want to strategically place teams at subway station entrances
to collect email addresses and those who sign up are sent free
tickets to the gala. 

Utilize the publically available MTA subway data to optimize the 
placement of the street teams. 
---
```

-----

# Contents

- [Introduction](#introduction)
  - [Goal](#goal)
  - [Questions to Answer](#questions-to-answer)
- [Data](#data)
- [Identifying the Best NY Regions](#identifying-the-best-ny-regions)
  - [Target Population](#target)
  - [Optimal Locations and Time](#optimal)
  	- [Manhattan](#manhattan)
  	- [Brooklyn](#brooklyn)
- [Conclusion](#conclusion)
  - [Divide and Conquer](#divide)
  - [Timing is Everything](#timing)

-----

# Introduction <a name="introduction"></a>

## A. Goal <a name="goal"></a>
* Increase **attendance** at the gala.
* Maximize **donations** to the organization.
* Drive **awareness** to the cause.

## B. Questions to Answer <a name="questions-to-answer"></a>
* **Who** is the target population?
* **Where** is the target population located?
* **When** are they most present?

-----

# Data <a name="data"></a>
* [NYC MTA Turnstile Data](http://web.mta.info/developers/turnstile.html)
* [US Census Data for NYC](https://www.census.gov/quickfacts/fact/table/kingscountybrooklynboroughnewyork,queenscountyqueensboroughnewyork,richmondcountystatenislandboroughnewyork,newyorkcountymanhattanboroughnewyork,bronxcountybronxboroughnewyork,newyorkcitynewyork/PST045219)

-----

# Identifying the Best NYC Regions

## A. Target Population <a name="target"></a>

1. Percentage of women was generally even across boroughs
<img src="{{ site.url }}/images/Percentageofwomen.png">


2. High number of women-owned firms in Manhattan, Brooklyn, Queens
<img src="{{ site.url }}/images/Women_Owned_Firms.png">


3. High median income in Manhattan, Staten Island, Queens
<img src="{{ site.url }}/images/Median_Income.png">

* Relaying back to the goals below for this gala, the team decided to focus on **Manhattan** and **Brooklyn**.
	1. Maximizing donations
	2. Driving awareness

	*As a note, Queens was also initially considered. However, Queens' traffic was significantly lower than Manhattan's and Brooklyn's, which did not meet the first goal of increasing attendance at the gala.*

## B. Optimal Locations and Time <a name="optimal"></a>

### Manhattan <a name="manhattan"></a>
	
1. Top 5 stations in Manhattan by total traffic
<img src="{{ site.url }}/images/Manhattan_Volume.png">

2. Weekdays have significantly more traffic than weekends
<img src="{{ site.url }}/images/Manhattan_Daily.png">

3. 8AM - 12PM and 4PM - 8PM time periods have the most traffic
<img src="{{ site.url }}/images/Manhattan_Hourly.png">

### Brooklyn <a name="brooklyn"></a>

1. Top 5 stations in Manhattan by total traffic
<img src="{{ site.url }}/images/Brooklyn_Volume.png">

2. Weekdays have significantly more traffic than weekends
<img src="{{ site.url }}/images/Brooklyn_Daily.png">

3. 8AM - 12PM and 4PM - 8PM time periods have the most traffic
<img src="{{ site.url }}/images/Brooklyn_Hourly.png">

-----

# Conclusion <a name="conclusion"></a>

## A. Divide and Conquer <a name="divide"></a>

Sending two teams, one to Manhattan and one to Brooklyn, will optimize the potential outreach based on foot traffic at subway stations across NYC.

	Manhattan Top 5:
	1. 34 ST Penn Station
	2. 34 ST Herald Square
	3. 23 ST
	4. 42 ST Port Authority
	5. 42 ST Times Square

	Brooklyn Top 5:
	1. 59 ST
	2. ATL AV / Barclay
	3. Jay ST / Metrotec
	4. Church AV
	5. Borough Hall

## B. Timing is Everything <a name="timing"></a>

Weekdays see significantly more traffic than weekends - specifically **Tuesday through Friday**.

During the day, stations are the busiest when people are commuting to and from work - specifically **8AM - 12PM** and **4PM - 8PM**.

