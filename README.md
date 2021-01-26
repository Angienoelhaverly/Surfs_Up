# Surfs_Up
*Use SQLAlchemy to connect to and query a SQLite database. Design a Flask Application to display our analysis on a website in real-time.* 

## Project Purpose
We have a business venture idea to open up a Surf 'n Shake shop that will serve ice cream and sell surfboards to locals and toursists in Hawaii. We need investor backing to start this venture. We've come up with our business proposal but our investor is concerned about the weather and we need to run analytics on a weather dataset for our business meeting. There should be just enough precipitation for a green environment, but not so much that the amount of rain hampers business by ruining ideal surf and ice cream weather. 

The analysis will focus on the temperature and rainfall for the past 7 years from 2010 to 2017, specifically for June and December, the two months that are apart enough to ensure that we have a good condition year-round. In order to have enough data, we analyze data from six weather stations in Oahu, Hawaii. 

### Goals
* Use SQLAlchemy to connect to and query a SQLite database
* Use statistics like minimum, maximum, and average to analyze data.
* Design a Flask application using data.

### Resources
* SQLite: SQLite is a version of SQL that lives on a computer or phone (local) so it's smaller, faster, and doesn't have users. SQLite is the most widely used database engine in the world. It is used in smart phones, computers, and applciations like ITunes and Photoshop.  
    * [Hawaii Weather Dataset (SQL File)](https://github.com/Angienoelhaverly/Surfs_Up/blob/main/hawaii2.sqlite)
* SQLAlchemy: SQLAlchemy is a query tool designed for SQLite and the integration of statistical analysis with dataframe analysis. 
    * [SQLAlchemy queries (Jupyter Notebook File)](https://github.com/Angienoelhaverly/Surfs_Up/blob/main/SurfsUp_Challenge.ipynb)
* Flask: To share our analysis with investors, we used Flask which is a webframework that uses Python to build web pages allowing us to share our findings in real time. Building a quick Flask website to display the data works well for investors because they are less interested in the code and more interested in what weather trends the code tells us. 
    * [Flask Visualization for Investors (Python File)](https://github.com/Angienoelhaverly/Surfs_Up/blob/main/app.py)

## Implementation Overview
### Code Objectives 
* Reflect Tables into SQLAlchemy ORM
* Perform Exploratory Climate Analysis
* Determine the Summary Statistics for June
* Determine the Summary Statistics for December

## Results
To perform our analysis, we wrote two queries that filtered our data on the measurement tables in our database to retrieve temperatures for the months of June and December over a ten year period. After getting these filters, we could then convert the temperatures to a list, create a dataframe out of the list, and then run summary statistics on the dataframe using a pandas function. After running a statistical analysis query on the database (df.describe) and filtering for temperatures in June and December over the last ten years, our descriptive statistic results can be found below. 

### *June Temperature Observations* 
* In June there are 1,700 records: the highest temperature recorded was 85 degrees and never went below 64 degrees. Temperatures in June seem to stay mainly in the 70s and the average temperature in June is 74.94 degrees.

![june temp stats](https://user-images.githubusercontent.com/73972332/105802442-0886b380-5f50-11eb-9478-d5e6e8874c0c.png)
### *December Temperature Observations* 
* In December there are 1,517 records: the highest temperature recorded was 83 degrees and the lowest temperature reached 56. Temperatures in June December get a little colder than June but only by about 10 degrees and still tend to to stay mainly in the very low 70s with the average temperature at 71.

![dec stats](https://user-images.githubusercontent.com/73972332/105802438-07558680-5f50-11eb-8363-7da9e5db6b64.png)

### Month to Month Outliers
We can easily chart a quick box plot to graphically see the differences between the two months and easily identify if there are any outliers. Examining the box plot below, we see that December clearly has some colder days and more outliers than June does, so between the two months, June would be more ideal for our business operations. This makes sense given that December's standard deviation is 3.75 while June's standard deviation is only 3.25. But the positive news is that the two months average temperatures (between the 25th and 75th quartiles) all fall between 86 and 65 degrees Farenheit. The ideal surfing/ice cream weather! 

## Summary - High Level Overview

### Hawaii is a great location 
After running our weather analysis, we conclude that Oahu, Hawaii would be the perfect location for a Surf n Ice Cream Shake Shack. Overall, the temperature on Oahu remains consistent at a comfortable range of 65°F to 85°F year-round. Based on temperature, Oahu would be an ideal location to open up a surf and shake shack. Below we can see that even with some rain, it would not be enough to hamper our ideal surf and ice cream weather. 

### Additional Queries
We can use the same procedure to compare the amount of rain (in inches) over the years as we did for temperature. Below are two additional queries that filter the precipitation levels for the months of June and December (focused on finding the summary statistics for each). Looking at the data below, we see that while there is definitely rain in Hawaii year round, the rain is not so abundant that it would hamper our ideal surf/ice cream weather. June tends to have less rain than December, but they are both still fairly agreeable months. 

#### *June Precipitation Observations* 
* Overall, June in Hawaii sees a max rainful of 4.43 inches with an average daily amount of .136 inches while 25% of the time, there is no rain at all. 
![june precip](https://user-images.githubusercontent.com/73972332/105912155-e50b4980-5fdf-11eb-96d3-eb52d9af031e.png)

#### *December Precipitation Observations* 
* Overall, December in Hawaii sees a max rainful of 6.42 inches with an average daily amount of .217 inches while 25% of the time, there is no rain at all.  
![dec precip](https://user-images.githubusercontent.com/73972332/105912195-f3596580-5fdf-11eb-8023-603b4d540616.png)


https://stackoverflow.com/questions/11616260/how-to-get-all-objects-with-a-date-that-fall-in-a-specific-month-sqlalchemy/31641488
