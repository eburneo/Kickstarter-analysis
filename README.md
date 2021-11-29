# An Analysis of Kickstarter Campaigns

## Overview of Project

Performing analysis on Kickstarter data to uncover trends.

### Purpose

Louise would like to know how different theater campaigns fared in relation to their launch dates and their funding goals. Using data from various other campaigns, we will help her visualize trends based on launch date and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To analyze the data for the outcomes of campaigns that were successful, failed, and cancelled by launched date, a pivot table and line chart were used. 

The following data points were used in the pivot table:

* A filter was included in the pivot table to allow Louise to select type of campaign in the Parent Category and Years. A new column "Years" was created using the data extracted from the "date Created Conversion" using the YEAR() function.
* The rows were formatted to show the months that corresponded to the "Date Created Conversion" column.
* The data from the "Outcomes" column was used in pivot table columns field and then filtered on 3 of the 4 fields: Successful, Failed, and Canceled.


![PivotTable](https://github.com/eburneo/Kickstarter-analysis/blob/main/Resources/PivotTable.png) ![PivotTables_Fields](https://github.com/eburneo/Kickstarter-analysis/blob/main/Resources/PivotTable_Fields.png)

### Analysis of Outcomes Based on Goals

To analyze the data for the outcomes based on goals, the percentage of successful, failed and canceled plays based on the funding goal was calculated. In order to do so, the number of successful, failed, and canceled projects for different goal amount ranges had to be counted. The CountIFs() function was used. 

![CountsIFS](https://github.com/eburneo/Kickstarter-analysis/blob/main/Resources/CountIFS.png)

### Challenges and Difficulties Encountered

- A challenge when using pivot tables was (potentially) understanding what data to select and in what fields to place that data in the pivot table. Also, formatting the rows labels to show only the month using the "Date Created Conversion" data was a bit challenging. I found several good resources using google. 
- The most challenging part of working with the CountIFs() was trying to keep the order of the column cells aligned with the range amount within the function argument. Towards the end, I realized that I could have anchored the cells and copied and pasted down for each outcome and just changed the range. I learned the hard way.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  1. The most successful theater campaigns were launched in May. Overall, theater campaigns launched between April through August did better than other months in the year. 
  2. Failed theater campaigns stayed consistent throughout the year regardless of launch date and were never exceeded the successful campaigns.

![Theater_Outcomes_vs_Launch](https://github.com/eburneo/Kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

- What can you conclude about the Outcomes based on Goals?

  - Fundraising was successful $1,000 or less & between $35,000 to $45,000. 
  - The outcomes based on goal are mirror opposites of other on the line graph

![Outcomes_vs_Goals](https://github.com/eburneo/Kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

- What are some limitations of this dataset?

  - A limitation of this data set could be potential outliers. We would need to identify those and then decide if we wanted to use them in the analysis.
  - Since I did not collect the data, the quality and format of the data may be a limitation.

- What are some other possible tables and/or graphs that we could create?

  - In addition to the line graphs created, we could also have created clustered or stacked columns graphs, bar graphs and even a pie graph.
