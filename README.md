Mini Data Case: Median Household Spending in Nigeria

I modeled the dataset with a logistic regression classification model. The target variable was 'median_spend', or the weighted average of median household spending. Since there was no indication of a particular business use case, this model could be applied for several goals, such as identifying homes with high spending to market for a commercial product or homes with low spending that may be at risk for socio-economic factors. I performed spatial autocorrelation (clustering spatial similarity as well as attribute similarity) on the target variable ('median_spend'). I computed the Moran statistic to identify hot and cold spots within the spatial data, which I converted into two categories, high spend and low spend. The model had an F1 score of 0.77 with an AUC score of 0.90, so the model performed quite well. I choose the F1 score as it is the harmonic mean of precision (the exactness) and recall (completeness). It takes into account false positives and false negatives. F1 is also better when there is a class imbalance, which was present for the high and low spend variables.

I explored and mapped the data in several ways. I found that the independent variables had weak correlations to the target variable (correlation matrix below). I also plotted each variable in a regression line plot to examine their linear relationships with the target variable. Several variables relating to distance had negative relationships with median_spend, indicating that the further the distance from ports, powerplants, accessibility to cities, transmission lines, and roads, the lower the median household spending in Nigeria. I did model the data with a ordinary least squares regression model. The R2 was 0.31, indicating that only 31% of the target variable can be explained by the predictor variables, which is worse than flipping a coin or guessing. With poor OLS model performance and weak correlation variables, I did not pursue a linear regression model further on this dataset.
