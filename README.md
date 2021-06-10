# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this analysis is to put together visualizations and insights on how different fundraising campaigns fared in relation to their launch dates and funding goals.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

This analysis was put together by first creating "years" column based on launch date to allow for an aggregated visualization of outcomes by month in a line chart. The line chart below is filtered to theatre related fundraisers category which includes plays, musicals, and spaces.  The years is also included in the filter however the chart in it's current form is showing all years.  It can be dynamically filtered by year in the source file.   The Y axis represents the count of the outcomes excluding those in "Live" status and the x axis is showing the month of fundraiser launch date.  The lines in the graph represent each out ccome including "Successful", "Failed", and "Cancelled".  Analyzing the chart visually provides an general view of outcomes over time and identifies seasonality.

![Chart1](https://github.com/sbretag/kickstarter-analysis/to/Theatre_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

This analysis was performed by creating a table with fundraising goal amounts grouped in buckets.  Each fundraising bucket was that broken down by the count of each outcome (excluding outcomes in "Live" status).  Additional calculations were added to show success/failure for each group as well.  In order to perform visualization analysis, the data was then charted in a line graph for each outcome showing % of total project count on the Y axis, the fundraising goal amount groups on the X axis.  Note that the data is limited to outcomes of theatre plays only.Analyzing the chart provides a general view of outcome performance across each goal amount bucket.

### Challenges and Difficulties Encountered

I didn't really run into any difficulties with this challenge however possible challenges could of been creating a countifs formula that had 4 different sets of criteria ranges/criteria including your max and min amounts of goal buckets, the different outcomes, and filtering on the plays subcategory.  To make it easier on myself, I created a secondary lookup table on the max/min dollar amounts for the goal buckets on a seperate table.  Typing in the max/min amounts in for each row opens up the door for typos.  I used a seperate lookup table on a secondary tab to stay within the first requirement of the second deliverable, a new sheet with 8 columns and 12 rows.  Otherwise I would of had them hidden in the first two columns.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

	1. There were more successful campaigns started in May than any other month.
	2. December had almost an equal amount of successful and failed campaigns.

- What can you conclude about the Outcomes based on Goals?
	1. Campaigns with goals $4,999 or lower (1st two groups) had success rates of 73.4% which is significantly higher than any other goal buckets with more than 6 projects.  
	2. Failure rates steadily increase with higher goal amounts when excluding less goal buckets with less than 7 projects.

- What are some limitations of this dataset?
	1. The sample size of data from the $25K to $29.9K bucket up through the greater than $50K bucket is relatively small.
	2. The $ buckets appear to be somewhat arbitrary, we could of possibly broken these out in quartiles instead. 
 

- What are some other possible tables and/or graphs that we could create?

	1. For outcomes based on launch date, filtering by all years helps with seasonality but prevents a trend view.  It might of been helpful to have a secondary chart with a trend over time by concatenating year/month over the X axis.  Alternatively, I could of maybe looked at using a stacked and grouped bar charts, showing the different years in the stack and grouping the stacked bars by outcome per each month.
        2. For the outcomes based on goals, I could of created box and whisker box plot on the detailed data set specifically to help indentify outliers and set goal buckets.

