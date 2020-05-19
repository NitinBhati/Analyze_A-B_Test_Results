# Analyze_A/B_Test_Results

A/B tests are very commonly performed by data analysts and data scientists. It is important that you get some practice working with the difficulties of these

For this project, I will be working to understand the results of an A/B test run by an e-commerce website. The goal is to work through this notebook to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

There is barely any difference in probabilities, p_converted_in_control Vs p_converted_in_treatment as they are almost equivalent to 12%. Hence, there is no concrete evidence suggesting that those who explore either page will neccessary lead to more conversions.

However, provided that all users in the Control group get the 'old page', and all users in the Treatment group get the 'new page', we will use the terms Old Page and New Page.

Using Bayes Rule we can find:

P(NewPage∣Converted)=P(NewPage)P(Converted∣NewPage))P(Converted)
 
Where:

P(Converted) = 0.1196
P(Converted | Old Page) = 0.1204
P(Converted | New Page) = 0.1188
P(New Page) = 0.5001


The value computed in part j. is called the p-value , and is used to determine whether the observed difference is statistically significant. If the p-value is < (less than) (typical) type I error rate of 5% (0.05), then this would suggest that there is a statistically significant difference, and we reject the null hypothesis.

However, with the computed p-value of 90% (> type 1 error rate of 0.05) this would suggest that there is no significant difference between the new and old pages; the new treatment page does not increase the conversion rate.

Having a large p-value say that the statistic is more likely to come from our null hypothesis; hence, there is no statistical evidence to reject the null hypothesis which states that old pages are the same or slightly better than the new pages.

The computed z-score of -1.3109 is less than the critical z-score of 1.645 for a one-tail test The computed p-value of 0.905 is greater than the critical p-value (type 1 error rate) of 0.05. There is no statistical evidence to reject the null hypothesis.

These findings suggest that there is no significant difference between the conversion rates of the old and new pages.


Since each row is either a conversion or no conversion which means the 'converted', is either a 0 or a 1, we will perform linear regression. However Logistic regression would fit too. But, either would work in this case as the dependent variable is 1. This approach is used when we are only trying to predict two potential/possible outcomes.


As per the OLS Regression Results: even after adding the ab_page there is no statistical evidence to indicate an impact on the conversion since p-values were all exceeding 0.05.

It does not appear that there is an interaction between page and country that has an impact on conversion.
