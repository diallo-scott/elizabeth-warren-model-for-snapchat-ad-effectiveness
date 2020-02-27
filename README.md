# Creating a Model for Impressions of Elizabeth Warren's Snapchat ads in 2019

## Multiple Linear Regression Model
Senator Elizabeth Warren was one of the top spenders amongst Snapchat politcal advertisers.  Thus, I thought it would be relevant to create a model that could determine how many impressions a Snapchat ad in 2019 would generate. I began with the business question: If I'm working as a marketing analyst for Elizabeth Warren, is it possible to determine which factors contribute most to the total impressions that a Snapchat ad gains?  If we can figure this out for 2019, then perhaps we can assume a similar model would uphold in 2020.

I would then need to determine which factors to investigate. For these factors I chose the amount spent on the ad, the number of ads ran within the same month, and the number of days the ad ran.  The amount spent and number of days the ad ran seemed to be obvious choices, since logically spening more should result in more impressions and an ad that runs longer has more days to make these impressions.  I then decided to add in the number of ads that ran within the same month, to see if having more ads running simultaneously would lead each individual ad to gain more impressions.  By combining these factors into a multiple linear regression model, I was able to create a fairly accurate model for how many impressions an ad that ran in 2019 would receive, and therefore how effective that ad was.

The result was the following model:

Number of impressions = 449.97 (Number of days ad ran) + 104.01 (Amount spent on advertisement) + 223.97 (Number ads in same month) - 31149.22

I was able to determine that my model was an accurate representation of reality by oberserving several values, including the R-squared, P-values, and F significance. The high value of R-squared, 0.997, tells us that our model can explain 99.7% of the data.  The low P-values (all of them are less than 0.0001) tell us that each of our independent variables are all related to the predicted output, and are each meaningful additions to our model.  Finally the extremely low value of F significance tells us that the joint effect of the three independent variables correlates very strongly with our output.

I would advise that this model would remain relatively accurate in the early part of 2020.  This is because all of Warren's 2019 Snapchat ads were ran in either November or December, so it would be fair to assume that not much has changed in the past two to three months.  An analyst using this model in period further removed from December 2019, should excercise caution, and note that the results may not have the same degree of accuracy that they did for the 2019 data.
 
## Simple Linear Regression Model
By creating a linear regression that took Senator Warren's spending on an ad and output the number of impressions, I hoped to see if there was a strong relationship between dollars spend and impressions gained.  The R-Squared value of 0.691, however, tells us that only 69% of the data could be explained by our model.  Thus we can see that there are other factors, besides spending on an advertisement, which contribute to the impressions it receives.  The chart depicting this regression is below.

![chartimage](https://github.com/diallo-scott/elizabeth-warren-model-for-snapchat-ad-effectiveness/blob/master/Simple%20Linear%20Regression.png)

## Step-by-step Data Manipulation
1. Apply filters columns of data
2. Filter the "PayingAdvertiserName" column to just include "Warren for President"
3. We now have just the ads paid for by Senator Warren and we copy it to a new tab "Warren Filtered Data"
4. We need to use text to columns to eliminate the extra characters behind Start and End dates.  We will use a space as the delimiter and choose to not import the column with the undesired information.
5. To generate the days from start to finish use the formula: =(Startdate - Enddate)
6. We now want to know how many other ads ran in the same month.  We first create a new column with just the month of the start date by using the formula =MONTH(Startdate cell)
7. We then use a countif formula to count how many other cells have the same month of start date.
8. We now create a pivot table to get the AdID, Spend, Number of Days Ran, Number of impressions and Number of Ads ran in same month formatted in a table. AdID is the row and the others are the values.
9. Use the Data Analysis toolpack to generate the multiple regression.  Make sure the Number of impressions is in the leftmost column and that the other columns (all except adID and number of impression) are selected as x-values (be sure to leave out the grand total row).  Then the number of impressions should be the y-value.  The proper multiple regression should be generated
10. To generate the single regression we copy paste the spend column and number of impressions column to a new spreadsheet and insert a scatterplot with a trendline.  Be sure to select that the equation and R-Squared value appear on the chart.

## Link to Excel Spreadsheet

https://github.com/diallo-scott/elizabeth-warren-model-for-snapchat-ad-effectiveness/blob/master/PoliticalAds.xlsx

## Link to Snapchat Data

https://www.snap.com/en-US/political-ads/





