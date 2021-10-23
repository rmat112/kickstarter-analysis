# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends.

## Overview of Project
Louise’s play Fever came close to its fundraising goal in a short amount of time. She wants to know how different campaigns fared in relation to their launch dates and their funding goals. 
### Purpose
The purpose of this analysis is to use the Kickstarter data and visualize campaign outcomes based on their launch dates and their funding goals.
## Analysis and Challenges
I conducted the following two types of analyses:
1. I analyzed campaign outcomes based on launch date. The campaign outcomes varied from "successful" to "failed" to "canceled".
2. I also analyzed outcomes based on Goals chart. I visualized the percentage of successful, failed, and canceled plays based on the funding goal amount. 

Click here to view my excel file: [Kickstarter_Challenge](https://github.com/rmat112/kickstarter-analysis/blob/main/Kickstarter_Challenge.xlsx)

### Analysis of Outcomes Based on Launch Date
- After renaming the StarterBook to Kickstarter_Challenge, added a column to the worksheet to extract the year from the “Date Created Conversion” column. This was done by using YEAR() function. 
- Then a pivot table was created in a new the sheet "Theater Outcomes by Launch Date". 
- Grouped the Row Labels column to show the months of the year. 
- Filtered the "Parent Category" to show only the data for "theater". 
- Created a line chart from the pivot table to visualize the relationship between outcomes and launch month. 
- This indicates that most successful campaigns were launched in the months of May and June. Also, the least successful or failed campaigns were launched between October and December.

 ![Theatr_Outcomes_vs_Launch](https://github.com/rmat112/kickstarter-analysis/blob/main/resources/Theatr_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
- Here I created a new sheet "Outcomes Based on Goals." 
- Used COUNTIFS() function to populate this sheet with "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created in Step 3, and on the "Subcategory" column using "plays" as the criteria.
- The SUM() function was utilized to calculate the "Total Projects" column.Then I calculated the percentages of successful, failed, and canceled projects based on the data from the "Total Projects," "Number Successful," "Number Failed," and "Number Canceled" columns. 
- Created a line chart for percentage of successful or failed projects.
- The chart shows an overall trend of decreasing number of successful campaigns with increasing goal amount. 

    ![Outcomes_vs_Goals](https://github.com/rmat112/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)
    
### Challenges and Difficulties Encountered
The only challenge I faced was during the application of COUNTIFS() function. Due to the use of several conditions in the formula I ran into some errors. However, upon close inspection I was able to find the errors in my formula and debug successfully.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  My conclusions about the outcomes based on launch date are as follows:
  1. Most of the successful campaigns were launched in the months of May and June. 
  2. Also, the least successful or failed campaigns were launched between October and December.

- What can you conclude about the Outcomes based on Goals?

  The number of successful campaigns decreases with increasing goal amount. Most number of successful campaigns were for a goal amount between $1,000 and $4,999.

- What are some limitations of this dataset?

  This dataset includes data from all over the world. Because of geographical disparity all data might not be applicable to Louise's case. So it would be better to use data from only the applicable geographic region.

- What are some other possible tables and/or graphs that we could create?
  - When analyzing the outcomes based on goals, plotting %successful and %failed on the same chart is not required because these two curves provide the same information (the sum of %successful and %failed is 100%). A chart with total number of successful campaigns would be more useful than % successful so that we can get a complete and correct picture. 
  - Analysis of failed campaigns can also be a useful tool to understand why and when some campaigns failed. I sorted the kickstarter data by "failed" outcome in "theater" category. Then I created a pivot table by "date of conversion" grouped by months and plotted against average donation and goal amount. I noticed that in May/June (when most campaigns were successful) even the failed campaigns got more average donation than their goal, but failed campaigns drastically fell short on funds during the months of December and April.
 
  ![Launch_vs_goal_avg-donation](https://github.com/rmat112/kickstarter-analysis/blob/main/resources/Launch_vs_goal_avg-donation.png)
