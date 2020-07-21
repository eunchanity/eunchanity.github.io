---
layout: post
title: Predicting Premier League Players' Salaries with Linear Regression
---

# Contents

- [Introduction](#introduction)
  - [Goal](#goal)
  - [Questions to Answer](#questions-to-answer)
- [Data](#data)
- [Selecting Quantitative Statistics](#stats)
- [Creating a Linear Regression Model](#model)
  - [Results](#results)
- [Key Takeaways](#takeaway)
  - [Top Statistics that Impact a Premier League Player's Salary](#topstats)
- [External Factors](#external)
- [Future Considerations](#future)
- [Link to Presentation](#link)

-----

# Introduction <a name="introduction"></a>

## A. Goal <a name="goal"></a>
* Conduct a **quantitative analysis** between player statistics and player salary
* Build a **linear regression model** that can predict a Premier League player's salary based on his stats
* Recognize other **external factors** that affect player salary

## B. Questions to Answer <a name="questions-to-answer"></a>
* Is there a relationship between a player's stats and a player's salary?
* Which quantitiative statistics affect a player's salary the most?
* Can a player's salary be accurately predicted?

-----

# Data <a name="data"></a>
* <a href="Premier League 2018-19 Player Data" target="_blank">https://fbref.com/en/comps/9/1889/2018-2019-Premier-League-Stats</a><br/>
* <a href="Premier Leauge 2018-19 Player Salaries" target="_blank">https://www.spotrac.com/epl/</a><br/>

-----

# Selecting Quantitative Statistics <a name="stats"></a>

* 9 player statistics were selected across 4 major categories:
	* Standard stats
	* Shooting stats
	* Passing stats
	* Possession stats

* The number of Premier League players in the 2018-19 season were narrowed down to just 383 players because the player never played in the Premier League and/or the player's salary was unavailable.

<img src="{{ site.url }}/images/premleaguestats.png">

-----

# Creating a Linear Regression Model <a name="model"></a>

* Machine learning algorithms were used to run the quantitative statistics through multiple regression models. <br/>
	* Essentially, the data was broken down into **train, validate, and test** sets so that a best-fit model could be identified.<br/>
	* After some fine tuning with different parameters, the model was then scored on how well its predictions were against the test set.

<img src="{{ site.url }}/images/crossvalidation.png">

## Results <a name="results"></a>

* The features (input variables) shown below were the ones that fit the model the best. 
	* *The starred features were log transformed to better fit the model.*

<img src="{{ site.url }}/images/coefindollar.png">

-----

# Key Takeaways <a name="takeaway"></a>

* The top statistics that affect a Premier League player's salary are ones that are generally associated with either **scoring more goals** or influencing a team's **likelihood of winning**. 
	* This makes sense - if a player helps you win more games, then you'd probably pay him a higher salary.

## Top Statistics that Impact a Premier League Player's Salary: <a name="topstats"></a>
	1. Shots on Target P90
	2. Goals P90
	3. Total Pass Completion P90

-----

# External Factors <a name="external"></a>

* There are factors outside of just the quantitative statistics that currently affect a player's salary. 

<img src="{{ site.url }}/images/externalfactors.png">

-----

# Future Considerations <a name="future"></a>

* Adding players that are not from the Premier League (i.e. La Liga, Bundesliga, Serie A, Ligue 1, etc.)
* Inputting even more quantitative statistics that are tracked per player.
* Research on a player's influence outside the game (i.e. marketability score)

-----

# Link to Presentation <a name="link"></a>
* <a href="Presentation PDF in Github" target="_blank">https://github.com/eunchanity/davids_repo/tree/master/projects/project2_premierleague_salary/reports</a><br/>