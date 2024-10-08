# PowerBi Report of Commissions Received by Korean Tour Agency

## Background

A lot of South Korean inbound tour agencies in Australia are structured in ways that heavily rely on commissions generated from their customers buying various goods at designated shopping centres. Therefore it is extremely crucial for the agencies to see the status of these commissions generated as they happen. It is widely known within the company that the 3 components: tour guide, tour itinerary/type of team and shop significantly affect the commission generated. This report will use these key 3 components in reviewing the company's performance.<br>
<br>

## How to use

1. Download both the excel file and the power bi file.
2. Change the data source in PowerBI to the excel file.
3. Power BI reads from the data and guide tab in the excel file. Other tabs were created to do other tasks.  


## Data Source

I have a modified version of the excel file it originally uses. So it is a dummy data. <br>

## Definitions

**Tour Code** contains follwing components in its code. First 6 letters consist of Types of itineraries, the next 6 letters consist of the tour's starting date, the remaining letters indicate the class of the tour.<br>

**Types of itineraries** means different variants of packaged tours. Different destinations/routes. <br> 

**Class** determines whether a team is a budget or more premium team. However, it isn't just 2 variants but many different variants of class.  <br>
<br>

## Walkthrough of the Report

### Overview

The demo seem to get an error in the first page. Here is the screenshot of what it's supposed to look like. 
[Overview Page](https://github.com/ys98110/Korean-tour-agency-powerBI/blob/main/overview_screenshot.PNG)

As the title suggests, this page is meant to show the user overall status of the commission generated. The page can be filtered by ranges of dates, shops, types of itineraries of the teams and the class of these teams. <br>


One of the most important KPIs that is widely used is the sales per head thus 3 of the visuals are related to this KPI. Going left to right and from up to down, we'll go through each of the visuals.

1. Simple sales per head calculation
2. Time series line graph of sales per head for each shop
3. The number of "adults" that is determined by the shops who are most likely or capable of buying goods. 
   1. This graph shows how many potential buyers have gone through the shop for different types of teams
4. It is widely known in the industry that the tour guides leading the tourists largely contribute to the amount of sales. Therefore, tour agencies tend to recruit high performing guides as their exclusive guides also known as House guides. This graph compares the performance of the House(exclusive) guides to Non-House (non-exclusive) guides.
5. This shows the total amount of commission generated by each guide for the set dates. It is sorted by the amount and this gives a slight idea into which guide the user should look further into.<br>

### Monthly

This shows a simple per month performance of different teams. 

### Guide Ranking

The purpose of this page is gain knowledge of which guide to further analyse. This page can be filtered by ranges of dates and shops. 

1. List of sales per head for each guide in different shops that is sorted by sales per head. 
2. Bar graph of total commissions generated by each guides.
3. Decomposition tree of number of adults handled that is decomposed of shop --> guide --> itinerary --> class<br>

### Guide

Now that the user knows which guide to look further at from the guide ranking page, user can now have further insight into the guide. This page can be filtered by ranges of dates and guides. It can also be further filtered by itinerary and shop if user clicks in one of the graphs. 

1. Bar graph of sales per head for each shop. This checks guide's overall performance for the current period. 
2. Time series of sales per head drawn with each line representing different shops. This checks the guide's performance over time how shows a little insight into how the figure in 1 was generated. 
3.  This table shows the average sales per head for house and non-house guides for each shops. This figure enables the user to review the relative performance of the guide.
4.  This number indicates how many teams the guide has handled for the given period. 
5.  This bar graph shows sales per head of each itinerary for each shop. This graph shows that the relative performance of the guide depending on different itinerary. 
6.  This stacked bar graph shows how many tourists were handled by the guide and taken to the shops for each itinerary and each bar is consists of the classes it belongs to. 
7.  This bar graphs shows the number of teams assigned to the guide.

Graphs 1,2,3 reviews the guide's performance and 5,6,7 reviews what type of teams the guide has been allocated with. This page gives full insights into the guide's performance and how this was generated.<br>

### Allocation

One of the mission critical tasks in the company is to assign guides to each teams that come through. One would want to allocate relatively "good" teams to better performing guides to maximise profit but this would leave other guides feel abandoned. 
It is a very delicate task and this graph shows what types of team each guides have been assigned with. 

### Shop

One of the key factors affecting the commission is the shops. The tour guides can lead tourists into being customers, but it's the shops' employees that ultimately seal the deal by making the tourists buy items.
This page gives an overall insight of the performance of each shop for the given period and it can be filtered by range of dates and shop. 

1. Bar graph of sales per head for each itinerary. 
2. Decomposition tree commission generated by itinerary and class.
<br>1,2 shows how the shops perform for different types of teams.<br>
3. Bar graph of sales per head for each shop. This compares the performance of the shops side by side.
4. Pie chart of the commission categorised by shop. This shows the company's relative dependance on each shop.
5. Table showing number of tourists the company allocated to visit each shop for the given period. 
6. Area chart showing commision and the sales generated by each shop. This gives an overall insight into the commission rate. 

This page analyses the overall performances of each of the shops and emphasises the difference in performance of individual itineraries, while comparing one shop to another. It also gives insight on how much resources (Number of guests) we allocate into each shop and how much commission it generates in return. 

### Distribution

As mentioned before, one KPIs we consistently use in this report for analysis is sales per head. It is a good indicator but it is extremely prone to outliers. The worst of the worst performing guides will have sales per head of 0 and this is the absolute bottom while the best performing guides can sky rocket the average sales per head without limit. Therefore, the overall sales per head is bound to be higher than a "normal" guide will have. <br>

To illustrate the wide spread of sales per head and other measures, boxplot of sales per head averages by Guide and Shop, histogram of number of adults per entry and histogram of commission generated per entry to give the user a better picture of the overall performance of the company. 

## Conclusion

This report tries to fully analyse and evaluate company's performance in generating commission from sales in designated shopping centres. As this data is a dummy dataset, I cannot conclude to any conclusion but I hope whoever is working in the industry with a similar business model can find this useful. <br>
<br>
ps <br>
Some things I wished to include in the report was the age, gender and products bought for each tourists. However, I did not have the suitable resources or the time to gather these data. Also the owner of the business did not require this much detail. (This report itself also included details he did not ask for but some he actually found useful)


