# LIFE-EXPECTANCY-PREDICTION
Started with fetching the data from the gapminder dataset, by performing inner join each time a new file was pulled. 
Inner join on first two files, and then its result’s inner join with third file and so on and so forth. Created a data frame out of it.

Then, wanted to perform prediction of life expectancy by linear regression model. So declared life expectancy as the Response Variable and 
the remaining ones as potential candidate Predictors.

The predictors are “Infant mortality rate (per 1,000 births)”, “Murder (per 100,000 people)”, “GDP per capita (US$ adjusted for inflation)”, 
“Medical doctors (per 1,000 people)”, “Poverty rate (people below $5.50 a day)”. Plotting each of the predictors against the Response Variable 
to determine which pair has the best fit of line or the best relationship or even coefficient correlation. Based on either factor, 
chose one to be the predictor of the linear model.

The Predictor chosen was “Infant mortality rate (per 1,000 births)” and built a linear regression model of these two with an RMSE value of 0.0128450506007272.
This model had some outliers which were removed to get an RMSE of 0.0115220444844038.

Added another potential candidate to the model based on the residuals of the existing model plotted against each candidate predictor and the one which was
evenly-roughly scattered, was chosen and added to the model which achieved an RMSE of 0.01008085.

Then, we exhausted all possibilities of different combinations of predictors with the response variable and based on their RMSE’s, picked the most suitable 
candidate at each step and made the model as perfectly predictable as possible. The point at which the RMSE of the model increases on picking any of the candidate,
we stop trying the possibilities and choose only the ones that we’ve come across till now.

In the end we have a perfect model ready to predict the life expectancy.
