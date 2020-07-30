--Module 1 Challenge-------------------------------------

# Kickstarting with Excel

## Overview of Project
### To analyze discrete dataset ("kickstarter") which contains goal and pledged dollar amounts for various startups.  In turn, these startups are broken down into Parent & Sub categorization to further help identify the relative success or failure of their efforts relative to each other.  
### For this specific analysis, we'll be looking at:
1. Campaign Outcomes of Theatre Events Based on Launch Date
2. Campaign Outcomes for Play Events Relative to their Target Goal

## Analysis and Challenges
For [Campaign Outcomes of Theatre Events Based on Launch Date](Theater_Outcomes_vs_Launch.png)
No significant challenge was encountered.  One minor event which could have been an issue would have been working from dataset with pre-existing filters in place.  Since the same dataset used for pre-lesson exercise was also used for the module challenge, it was important to remember to clear all pre-existing filters and not modify the original dataset.

For [Campaign Outcomes of Play Events Relative to their Target Goal](Outcomes_vs_Goals.png)
The most significant challenge was thinking of a shortcut to reduce excessive typing of the binned goals amounts.  Example, in the formula below, it would have been preferable to replace **<1000** with reference to a cell value containing the upper/lower bound of binned goal amount.
```
=COUNTIFS(kickstarter!$R$2:$R$4115,"plays",kickstarter!$F$2:$F$4115,"successful",kickstarter!$D$2:$D$4115,"<1000")
```
Another risk point of making a mistake would be copying this formula across the table to populate other columns.  In so doing, it would be important to remember to:
- Apply the **$** to fix the column/row being referenced in source data table 
- Update reference to binned goal amounts as well as successful versus failed result.

Finally, as a sanity check to confirm the calculation dropdown filter can be applied to the source table for a specific set of bin conditions to confirm an accurate COUNT calculaiton is taking place.

### Analysis of Outcomes Based on Launch Date
1. Best month for successful event should be targeted in the May~June timeframe.
2. Successful results consistently outnumbered Failed events except for the month of December.  Further analysis should be done to understand December's shortcomings.

### Analysis of Outcomes Based on Goals
1.  To guarantee a successful outcome, goal should be targeted at <$15,000.  Anything >$15,000 and their is variable risk where failed event outweighs successful events

For both of these analysis, "canceled" events had negligible impact.



## Results

Please note, this dataset was limited in scope to very specific analysis on Theater & Play events.  In order to widen scope of analysis, I would recommend comparison of these categories to all other present.  

This analysis was also very high level.  For further detail, it is recommended to go in depth for the observations already made.  For example, it would be good to understand why May~June were more successful than other events.  What specific events were taking place during this time?

Finally, in terms of time, further review can be done to identify specific days of the week which may be more successful than others.  Example, would we see higher success for events which took place on weekend (Friday/Saturday/Sunday) versus weekday (Monday~Thursday)?









--Module 1 Pre-Work Lesson-------------------------------------
# kickstarter-analysis [An Analysis of Kickstarter Campaigns]
Module 1 -- Excel -- Performing analysis on Kickstarter data to uncover trends.

This project focused on basic introduction to data analysis using Excel using a 4000+ row data representing kickstarter campaign donations from various geographical locations.
Topics covered: ---
* Pivot tables & charts ---
* Box Plots ---
* Mean, Median, Mode, Upper & Lower Quartile, IQR ---
* Variance & Standard Deviation ---
* Use of formulas for sheet navigation & data collection (vlookup, iferror) ---
* Conditional cell formatting, filters, sorting, text delimited column separation ---
