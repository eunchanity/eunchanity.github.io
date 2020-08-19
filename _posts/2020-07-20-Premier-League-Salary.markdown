---
layout: post
title: "Predicting Premier League Players' Salaries with Machine Learning"
date: 2020-07-17 13:32:20 +0300
description: Build a linear regression model to predict Premier League players' salaries using quantitative player statistics. # Add post description (optional)
img: manchester_united.jpg # Add image post (optional)
fig-caption: <a href="https://fbref.com/en/comps/9/1889/2018-2019-Premier-League-Stats" target="_blank">FB Ref - Premier League 2018-19 Player Data</a>
tags: [premier-league, machine-learning, linear-regression, salary]
---

# Introduction <a name="introduction">

A little background here, I am a die-hard Manchester United fan. I know for a fact that they make and spend a lot of money. In fact, the <b> average salary for a Manchester United player this season was \$7.6 million </b>. Crazy right? Now imagine my horror when I realized that this was the same team that placed 6th last year, 32 points behind the winners and bitter rivals Manchester City.

So I wanted to make this presentation for the premier league clubs and managers out there, in the hopes that they could invest their money more wisely. What better way to make this argument than through objective, quantitative statistics?

![In front of Old Trafford]({{site.baseurl}}/assets/img/manutd_stadium.jpg)

# Contents

- [Introduction](#introduction)
  - [Goals](#goal)
  - [Questions to Answer](#questions-to-answer)
- [Data](#data)
- [Creating a Regression Model](#model)
- [Results](#results)
- [External Factors](#external)
- [Future Considerations](#future)
- [So What?](#sowhat)
- [Link to Presentation](#link)

---

## Goals: <a name="goal"></a>

- Conduct a **quantitative analysis** between player statistics and player salary
- Build a **linear regression model** that can predict a Premier League player's salary based on his stats
- Recognize other **external factors** that affect player salary

## Questions to Answer: <a name="questions-to-answer"></a>

- Is there a relationship between a player's stats his salary?
- Which quantitiative statistics affect a player's salary the most?
- Can a player's salary be accurately predicted using machine learning?

---

# Data <a name="data"></a>

- <a href="https://fbref.com/en/comps/9/1889/2018-2019-Premier-League-Stats" target="_blank">FB Ref - Premier League 2018-19 Player Data</a>
- <a href="https://www.spotrac.com/epl/" target="_blank">Spotrac - Premier Leauge 2018-19 Player Salaries</a><br/>

Player statistics were scraped from www.fbref.com and player salaries were scraped from www.spotrac.com.

9 player statistics were selected across 4 major categories:

- <b>Standard</b>: general statistics for a player including goals, minutes played, assists, etc.
- <b>Shooting</b>: statistics focused on shooting including shots, shot percentage, free kicks, etc.
- <b>Passing</b>: statistics focused on passing including passes completed, total pass distance, etc.
- <b>Possession</b>: statistics focused on possession including touches, successful dribbles, pass target, etc.

Some of the tracked statistics were converted to a P90 (stat per 90 minutes) so that each player's ability is judged on a more balanced scale. The number of Premier League players in the 2018-19 season were narrowed down to just <b> 383 players out of a possible total of 577 players </b>. This is because the player either never played a minute of Premier League soccer and/or the player's salary was unavailable.

---

# Creating a Regression Model <a name="model"></a>

![Heatmap of Features]({{site.baseurl}}/assets/img/heatmap.png)

An initial baseline model was created to get a sense of how well the features (player statistics used to predict salary) predicted a player's salary without any tuning. Then, the data was run through multiple regression models including linear, polynomial, ridge, and lasso.

In the end, the <b>ridge regression model</b> provided the best R<sup>2</sup> test score:

> <span>R<sup>2</sup> test score: 0.520 </span>

> <span>Mean Squared Error (MSE): 0.14</span>

---

# Results <a name="results"></a>

![Salary Effects]({{site.baseurl}}/assets/img/premleague_salary.png)

The top statistics that affect a Premier League player's salary are ones that are generally associated with either <b>scoring more goals</b> or influencing a team's <b>likelihood of winning</b>. This makes sense - if a player helps you win more games, then you'd probably pay him a higher salary.

Top Statistics that Impact a Premier League Player's Salary:

> 1.  Shots on Target P90
> 2.  Goals P90
> 3.  Total Pass Completion P90

---

# External Factors <a name="external"></a>

Currently, there are factors beyond the stats that affect a player’s salary. <br/>

- For example, <b>richer clubs</b> show drastic differences in revenues, which then affects how well the clubs can pay their players.

- Also, a player’s <b>marketability</b> can vastly influence his salary. If a player is widely popular with teh fans, the club can afford to pay him a higher salary knowing that they can recoup that money from merchandising, licensing, etc.

- The <b>volatility of the transfer market</b> can also widely affect a player’s market value, which in turn affects his salary. For example, Pre-COVID19, the market was booming and this allowed PSG to purchase Neymar from FC Barcelona for $263 million, with an annual salary of $53m. However, as of now, clubs are unable to splash the cash and thus, unable to pay high salaries.

---

# Future Considerations <a name="future"></a>

- Adding players that are not from the Premier League (i.e. La Liga, Bundesliga, Serie A, Ligue 1, etc.)
- Inputting even more quantitative statistics that are tracked per player.
- Research on a player's influence outside the game (i.e. marketability score)

---

# So What? <a name="sowhat"></a>

The method that I’m proposing is one that is <b>driven by quantitative analysis</b>. If a salary is determined solely by tracked stats and a player’s performance, this could be a great way to standardize how a player’s salary is determined. Currently, salaries are negotiated between a player’s agent and the club. Since so much of this process is unclear, salary inequality often has a negative impact on a team. By standardizing salary negotiations, clubs can avoid overpaying on the market and spending millions on unfruitful gambles.

---

# Link to Presentation <a name="link"></a>

- <a href="https://github.com/eunchanity/davids_repo/blob/master/projects/project2_premierleague_salary/reports/project2_premleague_salary.pdf" target="_blank">Presentation PDF in Github</a><br/>
