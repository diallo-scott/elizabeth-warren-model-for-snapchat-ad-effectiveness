# Creating a Model for Impressions of Elizabeth Warren's Snapchat ads in 2019

## Multiple Linear Regression Model
Senator Elizabeth Warren was one of the top spenders amongst Snapchat politcal advertisers.  Thus, I thought it would be relevant to create a model that could determine how many impressions an ad in 2019 would generate. I began with the business question: If I'm working as a marketing analyst for Elizabeth Warren, is it possible to determine which factors contribute most to the total impressions that an ad makes?  If we can figure this out for 2019, then perhaps we can assume a similar model would uphold in 2020.

I would then need to determine which factors to investigate. For these factors I chose the amount spent on the ad, the number of ads ran within the same month, and the number of days the ad ran.  The amount spent and number of days the ad ran seemed to be obvious choices, since logically spening more should result in more impressions and an ad that runs longer has more days to make these impressions.  I then decided to add in the number of ads that ran within the same month, to see if having more ads running simultaneously would lead each individual ad to gain more impressions.  By combining these factors into a multiple linear regression model, I was able to create a fairly accurate model for how many impressions an ad that ran in 2019 would receive, and therefore how effective that ad was.

The result was the following model:

Number of impressions = 449.97 (Number of days ad ran) + 104.01 (Amount spent on advertisement) + 223.97 (Number ads in same month) - 31149.22

I was able to determine that my model was an accurate representation of reality by oberserving several values, including the R-squared, P-values, and F significance. The high value of R-squared, 0.997, tells us that our model can explain 99.7% of the data.  The low P-values (all of them are less than 0.0001) tell us that each of our independent variables are all related to the predicted output, and are each meaningful additions to our model.  Finally the extremely low value of F significance tells us that the joint effect of the three independent variables correlates very strongly with our output.
 
## Simple Linear Regression Model
By creating a linear regression that took Senator Warren's spending on an ad and output the number of impressions, I hoped to see if there was a strong relationship between dollars spend and impressions gained.  The R-Squared value of 0.691, however, tells us that only 69% of the data could be explained by our model.  Thus we can see that there are other factors, besides spending on an advertisement, which contribute to the impressions it receives.  The chart depicting this regression is below.

![chartimage](https://github.com/diallo-scott/elizabeth-warren-model-for-snapchat-ad-effectiveness/blob/master/Simple%20Linear%20Regression.png)




