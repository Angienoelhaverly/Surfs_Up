# Surfs_Up
*Use SQLAlchemy to connect to and query a SQLite database. Design a Flask Application to display our analysis on a website in real-time.* 

## Project Purpose
We have a business venture idea to open up a Surf 'n Shake shop that will serve ice cream and sell surfboards to locals and toursists in Hawaii. We need investor backing to start this venture. We've come up with our business proposal but our investor is concerned about the weather (mainly levels of precipitation) and we need to run analytics on a weather dataset from SQLite for our business meeting. There should be just enough precipitation for a green environment, but not so much that the amount of rain hampers business by ruining ideal surf and ice cream weather. The analysis will focus on the temperature and rainfall for the past 7 years from 2010 to 2017, specifically for June and December, the two months that are apart enough to ensure that we have a good condition year-round. In order to have enough data, we analyze data from six weather stations in Oahu, Hawaii. The analysis consists of two parts:
* Temperature analysis for June and December from 2010 to 2017
* Rainfall analysis for June and December from 2010 to 2017

## Goals
* Use SQLAlchemy to connect to and query a SQLite database
* Use statistics like minimum, maximum, and average to analyze data.
* Design a Flask application using data.

## Why SQLite
SQLite is a version of SQL that lives on a computer or phone (local) so it's smaller, faster, and doesn't have users. SQLite is the most widely used database engine in the world. It is used in smart phones, computers, and applciations like ITunes and Photoshop. Local databases support quick testing and prototyping. So SQLite helps turn things around more quickly. SQLAlchemy is a query tool designed for SQLite and the integration of statistical analysis with dataframe analysis. To share our analysis, we will use Flask which is a webframework that uses Python to build web pages allowing us to share our findings in real time. All SQLite databases are flat files, which means that they don't have relationships that connect the data to anything else. As a result, flat files can be stored locally, which will help us move more quickly through the analysis.
