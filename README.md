### Indian-air-quality-analysis

Air Pollution refers to the release of pollutants into the air that has adverse effect on human health and the planet as a whole. Today air pollution has been one of the significant problems to deal with for any nation. We have tried to analyze Indian air quality data to find some underlying principles or patterns which might give us an insight into how severe the problem is.

The main features that we used in our dataset is the concentration of gases like so2, no2 and rspm and spm.

As a part of preprocessing, we removed all those columns that were unnecessary for our model building and prediction. For data visualization we have used state feature but for building model we have removed the feature. We have removed agency name, stn_code, location_monitoring_station, state columns from our dataset. We have also remived the type feature that also is redundant for our analysis as it classifies the pollution as industrial, residential or other. We have checked for null, missing and duplicate values. The null values have been filled with the mean of their columns and columns with few null values have been dropped.
We plotted barplot, heatmap, and point plots as a part of data visualization. This also helped us to visualise outliers in our data.
It was clear from the correlation matrix that we have some correlation between spm and rspm.

In the barplot that was constructed using states and concentration of so2 we saw that so2 level is highest in Uttarakhand and lowest in Chandigarh

For building models using our dataset we have considered concentration of nitrogen dioxide, rspm and spm as independent variables and concentration of sulphur dioxide is been chosen as dependent variable.
The dataset has been split into training and testing sets with test size of 0.33. 
We have build linear regression, XGBoost regressor, lasso regression, Random forest and decision tree regressor in order to analyse the accuracy of different models on our dataset. 
We have analysed the accuracy of our models with the help of r sqaure values that we obtained for each of these models for our dataset. 
R2 is a statistic that will give some information about the goodness of fit of a model.
The R2 coefficient of determination is a statistical measure of how well the regression predictions approximate the real data points.

For linear regression, we have got an r square value of 0.1131 for training dataset and 0.11842 for testing dataset
For Lasso regression the values obtained were similar to that of linear regression.
By this we can conclude that linear and lasso models have similar r2 values for our dataset.
For random forest regressor, r square is 0.6005 for training dataset and 0.1393 for testing dataset
For XGBoost regressor, r2 value is 0.6420
For decision tree regressor, its 0.125 for both testing and training datasets

Since the r2 value of 1 indicates that the regression predictions perfectly fit the data, we can conclude that XGBoost has best performance out of all these models for our dataset with an r2 value of 0.6420.
XGBoost stands for eXtreme Gradient Boosting.
XGBoost is an implementation of gradient boosting decision trees designed for speed and performance. Gradient boosting is an approach where new models are created that predict the residuals or errors of prior models and then added together to make the final prediction. 

The analysis was purely data-driven, however, was backed by real-life instances. It is interesting to see how data analysis and the day to day instances are coherent and how data analysis can be used to deal with significant problems. Not only India but other countries are also suffering from air pollution.
We must find a cure to this significant problem as it is killing our nation slowly.

