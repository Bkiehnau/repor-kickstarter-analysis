# Kickstarting with Excel

## Overview of Project
Theater Outcomes by Launch Date and Outcomes Based on Goals

### Purpose
The purpose of this project was to practice excel skills learned in module 1 of this course by utilizing the kickstarter data provided. The specific purpose of this project was to show Theater Outcomes by Launch Date by creating a pivot table from the kickstarter data set provided. With this pivot table we were tasked to create a pivot chart, specifically a line graph, to visually represent our findings. After this initial task was completed, we were tasked to find Play Outcomes based on Goals. To provide this data we were asked to utilize our skills in counties functions, sum functions and classic division functions. Using these functions we were asked to provide the number of successful, failed and canceled projects based on specific thresholds I will provide below. After finding these numbers we were tasked to provide the percentage successful, failed and canceled. Once all data was compiled we were tasked to again provide a line graph to represent the project success statuses by percent. 

## Analysis and Challenges

### Analysis of Outcomes Based by Launch Date
In the analysis of outcomes by launch date tab I created a pivot table by clicking the insert ribbon tab and then clicking tables and pivot table. I then highlighted all data on the kickstarter excel tab, making sure to include the newly created years column where I found what year each kickstarter was launched. I did this by using the =Year() function in excel and referencing my column S, Date Created Conversion. Once I had my pivot table I put the Parents category and years data in the filters. I then put outcomes in the columns space and the values space. Additionally, I used date created conversion for my rows, getting rid of years and quarters so only the months were displayed. From the data that was now presented in my pivot table, I created a line graph pivot chart to display theater outcomes based on launch date. The chart is provided as an attachment in this repository named Theater_Outcomes_vs_Launch.png. I did not have much difficulty in this deliverable, but some challenges could be deciding what data sources to use for columns and rows in order to present the best data requested. There could also be some challenges in locating the insert pivot table function if someone is not familiar with excel.

### Analysis of Outcomes Based on Goals
For the second deliverable of our challenge we were tasked with using the countifs function to get the number of successful, failed and canceled play kickstarters by thresholds that I will list below.
Less than 1000
1000 to 4999
5000 to 9999
10000 to 14999
15000 to 19999
20000 to 24999
25000 to 29999
30000 to 34999
35000 to 39999
40000 to 44999
45000 to 49999
50000 or More
In order to find these thresholds I had to utilize a countifs function to filter data by successful plays. (I will focus of successful data while sharing my functions.) Two examples of functions that I used to get successful play data are as follows =COUNTIFS(Kickstarter!$F:$F,A17,Kickstarter!$R:$R,A20,Kickstarter!$D:$D,"<1000") for successful play counts less than 1000 and =COUNTIFS(Kickstarter!$F:$F,$A$17,Kickstarter!$R:$R,$A$20,Kickstarter!$D:$D,">=35000",Kickstarter!$D:$D,"<40000") for successful play counts from 35000 to 39999. Once I had all data for successful, failed and canceled play counts I summed the total projects by using a simple =sum() function. Next we were tasked with getting the percentages of successful, failed and canceled projects compared to the totals of each threshold. In order to do this I took the count of successful plays for a certain threshold divided by the total count of each threshold (successful, failed and canceled). An example of this function is =("successful less than 1000"/"total projects less than 1000"). After all data was compiled I then highlighted the Goal column and the Percentage Successful, Percentage Failed and Percentage Canceled columns. With these columns highlighted I inserted a line graph to represent outcomes vs goals by threshold. The chart will be attached to the repository with the title Outcomes_VS_Goals.png.

### Challenges and Difficulties Encountered
The only challenge I encountered in this deliverable was the creation of my counties function. I created my functions and knew I had all the necessary components, but my formula would keep giving me a 0 in each field. I used a function that follows, =COUNTIFS(Kickstarter!$F:$F,$A$17,Kickstarter!$R:$R,$A$20,Kickstarter!$D:$D,>=5000,Kickstarter!$D:$D,<10000). After about 30 minutes of internal strife and possibly a few cuss words I realized I needed to surround my threshold values in quotes. I changed my function to =COUNTIFS(Kickstarter!$F:$F,$A$17,Kickstarter!$R:$R,$A$20,Kickstarter!$D:$D,">=5000",Kickstarter!$D:$D,"<10000") and finally have my data appear. It just shows that you can have small missing components break an otherwise flawless function.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Conclusion 1 - Theaters have minimal canceled kickstarters each month.
Conclusion 2 - Late spring (May and June) hold the highest number of kickstarters that are both successful and failed, but specifically successful.

- What can you conclude about the Outcomes based on Goals?
Conclusion - Since there were no canceled play kickstarters, the percentage of successful and failed play kickstarters by threshold are directly inverse of each other.

- What are some limitations of this dataset?
I think that a major limitation to the datasets we created is that we did not take into consideration geographical area. We have a country column that we could have used for filtering our data down even further. It is possible that Each category could have drastically different success rates based by country. 

- What are some other possible tables and/or graphs that we could create?
For deliverable 2 a stacked bar graph would have been an adequate way to represent the data.
For deliverable 1 another bar graph would have been sufficient to represent the data as well.

