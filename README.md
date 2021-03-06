# Analysis of Factors Influencing Kickstarter Crowdfunding Campaigns in Theater
## Overview of Project
### Purpose
The goal of this project is to perform analysis on existing crowdfunding campaigns to uncover trend in successful campaigns based on various factors especially in theatre area in order to help Louise fundraising her play Fever with a goal of $10,000. We will use crowdfunding data from Kickstarter to analyze and determine the factors leading to successful campaigns, specifically how launch dates and funding goals can impact results of different campaigns.  
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
Crowdfunding data was obtained from Kickstarter website for crowdfunding campaigns from between 2009 to 2017. In the Kickstarter worksheet data set, date and year of launch date was calculated from Unix Timestamps from “Launched_at” column.  A new column of “Date Created Conversion” was created and the date of each launch date was converted from timestamps to day-month-year format. A new “Years” column was created to extract the yar from the “Date Created Conversion” column. To analyze outcomes based on date, a pivot table was created from the Kickstarter worksheet in new sheet “Theater Outcomes by Launch Date”. The Pivot table was filtered based on “Parent Category” and “Years”. Pivot table field was reported based on Outcomes and Date Created Conversion. By filtering only theatre and outcomes based on successful, failed and canceled, we created a pivot table of Kickstarter campaign in theater based on months between 2009 to 2017 as following: 

![Pivot_table1](/Resources/Pivot_table1.png)

A line chart was created from the pivot table to visualize the relationship between theater campaign outcomes and launch month, shown in figure below.

![Theater_Outcomes_vs_luanch]( /Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To analyze Kickstarter campaign outcomes based on funding goals, percentage of successful, failed and canceled plays was calculated based on the funding goal amount. A new sheet was created and named “Outcomes Based on Goals”. Dollar amount ranges with interval of $5000 was created to group campaign based on the goal amount, shown in the following figure.

![table2](/Resources/table2.png)

COUNTIFS function was used to populate number of successful, failed and canceled plays from outcomes within each specific range and percentage of successful, failed and canceled play among all plays are calculated for each dollar amount range as shown in table above.
Percentage of successful, failed and canceled plays over amount ranges of campaign goal is visualized by creating a line chart with amount range on the x-axis and percentage of project outcomes on the y-axis.

![Outcomes_vs_Goals](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
No difficulties were encountered during analysis. Some possible challenges encountered are obtaining the well representative crowdfunding data to help planning Louise’s campaign for her play.  There are many crowdfunding websites to choose from and to avoid drowning in data, we decided to use Kickstarter as representative site as it is the most famous one especially for creative entrepreneurs. 
## Results
- What are two conclusions you can draw about the Outcomes based on Launch Date?
  1. Based on the line chart of campaign outcomes based on launch month from 2009 to 2017, campaigns for theater are overall very successful. There are generally more successful campaigns than failed campaigns all year round except December.  
  2. Number of successful and failed campaigns follows a similar trend from January to December, but number of successful campaigns increased significantly starting May and the spike deceases by the end of the year. It suggests May is the best time to start a campaign with the best success rate over failure.
- What can you conclude about the Outcomes based on Goals?
  1. The percentage of successful plays versus failed plays from 2009 to 2017 varies according to the amount of fundraising goals. Campaigns for plays have higher success rate when funding goal is under $15,000 or between $35,000 to $40,000. The highest percentage of successful outcome is under 5,000 and the rate of success deceases with increasing amount of funding goals. Based on the data, it is recommended for Louise to keep her goal under $5,000 for best chance of success or at least under $15,000 for 10% better chance of getting funded.
- What are some limitations of this dataset?
  - Limitations of this dataset include time of the crowdfunding campaign and limited sources. The dataset is for crowdfunding campaign from 2009 to 2017 from Kickstarter. Firstly, for her to get a more updated dataset, it would be better to have a more recent data (from 2017 to 2021) to reflect on recent crowdfunding campaigns to help her mirror the success from project in the same category. Secondly, the dataset is limited to Kickstarter, one of the most popular crowdfunding platforms. However, there are other popular crowdfunding websites like Indiegogo, Patreon and GoFundMe. Other dataset from alternative platform could give a more generalized view of crowdfunding success. 
- What are some other possible tables and/or graphs that we could create?
  - For helping with Louise’s Play in US, we can focus on data for successful and failed campaigns in US by goals and launch date. Additionally, we should investigate the distribution of our data in campaign goals. Measure of central tendency and measure of spread can be calculated by creating table to show the mean, median, standard deviation, quartiles and interquartile range of the successful and failed campaign based on goals and pledged to have a better understanding of the successful amount of goals. We can also create box and whisker plots to show the distribution of campaign goals to identify potential outliers that could mislead the whole data analysis. 
