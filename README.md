# Kickstarting with Excel

## Overview of Project
**Task:** Project will analyze how different kickstarting campaigns fair in relation to their launch dates and their funding goals. 
* *The project uses the "Kickstarter" dataset previously presented in this branch to present a visual representation for its analysis/outcome/conclusion of the proposed task.* 

### Purpose
  This project aims to help the user practice certain Microsoft Excel skills and formulas as tools to create a visual representation of a data set given - namely "Kickstarter".

  Given certain contraints, the user has to manouver Excel to reach certain graphs/tables and analyze these to give a conclusion and answer the task presented in the Overview of the Project.
  The purpose of the project is also to:
> "inform Louise on how different kickstarting campaings fair in relation to their launch dates and their funding goals"

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date
___
  **Outcomes Based on Launch Date** was made by pivoting the 3 campaign outcomes *- successful, failed, canceled -* against the launch date *- month in this case -* 
of the theaters. 

Using the Excel function **YEAR()**, a new column **Years** was created in the *"Kickstarter"* sheet. Once pivoted, this column allowed for the display of the months on the X-axis of the Pivot Chart below against the total number of theaters on the Y-axis.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/89520192/131281366-48c4ba45-64bd-4943-8e7b-c5866e944d2b.png)

We can see that the months of May and June had the highest total number of successful theater launches, while the month of December had the lowest. It is also interesting to note that during December, almost as many theaters failed as were successful, which can be interpretted as a 50% chance of failure. 

The graph shows us the difference between how many theaters failed vs. succeeded. We can observe that the period of May-Jul had the highest gap between successful and failed venues. Another observation is that more theaters failed during October compared to the rest of the year, month during which no theaters were canceled. The margin between successful/failed theaters that month is not very high, which could suggest that it is better to cancel any non-promising opportunities early rather than taking a more probable loss. 
    
All together, the Pivot Chart displays an easy to understand theater outcome number total based on the launch date presented by month.  

### Analysis of Outcomes Based on Goals
___
**Outcomes Based on Goal** was made by creating and populating a 8x12 table. This table utilized the COUNTIFS() Excel formula to pull the number of theater outcomes (successful, failed, canceled) from the main
"Kickstarter" sheet based on the Goal number set in column 1, as well as the Subcategory "plays". 

Together, these 3 constraints (goal/outcome/subcategory-plays) arranged the number of theaters that were either successful/failed/canceled based on the monetary ($) goal presented. A simple SUM() formula was used to total each row of theaters by goal. 

From here, by dividing Number Successful/Failed/Canceled by its corresponding row total, the percentage was obtained. This percentage (%) was then graphed (below) using a line graph to show the final result of outcomes based on goal. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/89520192/131281662-64591e47-6bea-4c09-834e-7ad46af30989.png)

According to the graph presented, more than 50% of theaters were successful with goals ranging between (Less Than 1000) and (15000 to 19999). More than 50% of theaters with goals set between (20000 to 24999) and (30000 to 34999) failed, while 67% of theaters with goals between (35000 to 39999) and (40000 to 44999) succeeded. More than 88% (up to 100%) of theaters with goals above 45000 failed. 

### Challenges and Difficulties Encountered
---
**Challenges:**
No challenges were encountered during the creation of either of the two analyses mentioned above. *Possible* challenges that could be encountered during a task like these could be:
- Innaccurately placing the PivotTable Fields in their respective areas; If a field is placed in the incorrect area, the Pivot Table for Theater Outcomes Based on Launch Date will show different data 
from what is required, which in turn would change the outlook of the Pivot Chart presented.
- Missing one of the criteria ranges in the COUNTIFS() formula. This would result in the formula giving innaccurate # of projects, which would throw off the percentages and in turn inccorectly display the
data in the table.
- Misspelling any of the formulas used in the above analyses. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Conclusion 1: The month of December presents low numbers of success on top of a 50% of failure.
Conclusion 2: According to the data, the months of May and June have the highest numbers of successful theaters, so one is likely to have better results opening a venue during these months.  

- What can you conclude about the Outcomes based on Goals?
Conclusion: Goals ranging from less than 1000 to 15000 have a higher percentage of succesful theater launches, so in conclusion one should set their maximum goal no larger than 15000.

- What are some limitations of this dataset?
 
1. Not enough of a large pool of theaters to make generalizations based off the presented trends.
2. Not enough variable calculation of available plays/actors at certain times of the year which influence success/failure for different months.
3. Data could be incomplete, as some missing theaters might have not been accounted for, which limits the usability of this analysis.   

- What are some other possible tables and/or graphs that we could create?

Could have created a box and whisker graph showing the difference in average numbers of theaters used for this study. At the same time, we could have defined our current graphs more accurately to include the numbers of theaters used per each goal. 

For example, the 1000 to 4999 range had a total number of 534 projects used for this data, while the 45000 to 49999 goal had only 1 project. This theater failed and in doing so, caused the line on the graph to plummit at this specific instance. From an outside overview, without having more insight into what the data set used is made up of, this would make one belive that theaters with goals above 45000 are 100% likely to fail, however we cannot be certain of that with only a single example used in our analysis. 
