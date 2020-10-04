# kickstarter-analysis

## Overview of Project
An analysis of Kickerstarter launch dates, funding goals and the rate of success for those campaigns.

### Purpose
The client Louise fundraising campaign nearly completed the goal in a short peroid of time.  She now wants to analysis how different campaigns fared in relation to their launch date and funding goals.  

### Analysis and Challenges
To begin the anaylsis, I began by extracting the year from the column "Date Created Conversion".  I then created a pivot table (Outcomes Based on Launch Date) using the following settings:

- Sort: Parent Category
- Value: Count of Outcomes
- X axis - Outcome
- Y axis - Date Created Conversion

I the sorted the selected data by Parent Category: theater.  I created a line graph using this pivot table.
![Theater_Outcomes_vs_Launch](https://github.com/abiwat/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

I then created a sheet titled Outcomes Based on Goals.  Titled columns to hold data: 

- Goal
- Number Successful
- Number Failed
- Number Cancaled
- Total Projects
- Percentage Successful
- Percentage Failed
- Percentage Canceled.  

In the Goal column, labeled rows as follows:

Less than 1000
- 1000 to 499
- 5000 to 9999
- 10000 to 14999
- 15000 to 19999
- 20000 to 24999
- 25000 to 29999
- 30000 to 34999
- 35000 to 39999
- 40000 to 44999
- 45000 to 49999
- Greater than 50000.  

Created equation for each value range using COUNTIFS() for successful, failed, canceled for the play subcategory.  In the Total Project column I used SUM(), adding the number of successful, failed, and canceled for each category.   I then calculated the percentage of successful, failed and canceled projects using the formula =(number of successful projects/total number of projects).  I then categorized the column as percentage in excel.  I created a line chart in another sheet using the percentage of successful, failed and canceled projects. 
![Outcomes_vs_Goals](https://github.com/abiwat/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Analysis of Outcomes Based on Launch Date
Based on the data, April, May and June appear to be the optimal months to launch a theater kickstarter.  The months of September, October and November appear to be the least successful months to launch a project.

### Analysis of Outcomes Based on Goals
From this line plot, we can see that campaigns with goals lower than 9999 dollars were more likely to succeed than those projects with goals between 15000 and 34999 dollars.  Oddly enough, projects between 35000 and 44999 dollars seem to have a a better chance of succeeding.  Campaigns with goals greater than 45000 dollars are likely to fail.

### Challenges and Difficulties Encountered
There weren't any challenges or difficulties with this analysis.  The requested analysis was straight forward and the data was well organized and tidy.  

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Fundraising campaigns started in the spring (April, May or June) are likely to succeed.  Campaigns launched in the fall or winter (Septmeber, October and November) are likely to fail.

- What can you conclude about the Outcomes based on Goals?
Goals less than 9999 dollars are far more likley to succeed that campaigns with high goals.

- What are some limitations of this dataset?
For analyizing data relating to theatre and plays, additional data one whether the campaign is simple to put on a production of a play, or if it is to refrubish a theatre house.  More specific location data would also be useful, knowing if a play was successfully funded in New York City or in Fargo, North Dekota would provide useful geographical data to create a map. Knowing how the donars were directed the fundraising campaign would provide useful data as well.  

- What are some other possible tables and/or graphs that we could create?
A charter to determine the rate of success or failure if the campaign was in the 'spotlight'.  Compare average donations based on the goal for fundraising.  

