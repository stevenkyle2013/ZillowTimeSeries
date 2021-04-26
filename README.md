# Analysis of Idaho Housing Market
By: Steven Kyle

## Aim
The goal of this analysis is to find the top 5 zipcodes to invest properties in.


## Data
- The data that was used was provided by Zillow.
- It has entries from 14,723 zipcodes and spans 51 "States" (Includes D.C.)
- The dataset provides median housing prices for each month from April 1996-April 2018

## Workflow
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/Workflow.png" width="500">


## Chosen State: Idaho
Narrowed down the state to Idaho. Idaho reportedly has had the biggest growth in population as well as an influx of people moving to the state.

Based off of:
- U.S. News (Population growth of 2.12%, based off of 2020 census data)
  - https://www.usnews.com/news/best-states/slideshows/these-are-the-10-fastest-growing-states-in-america
- United Van Lines 2020 Study (70% inbound migration)
  - https://www.unitedvanlines.com/newsroom/movers-study-2020
- Hire a Helper Migration Report (Twice as many people moving in than out 2020)
  - https://www.hireahelper.com/moving-statistics/migration-report/

Requirements for Idaho zipcodes:
- Must have 10 years worth of data (Wanting to look at more established communities)

Idaho data:
- Original: 110 zipcodes
- Meeting Requirements: 108 zipcodes
- Used latest historic 5 year ROI to narrow down zipcodes to 25

This is a map of the 110 zipcodes that we have data on. The color indicates the latest historic 5 year ROI.
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/IdahoZips.png" width="500">

## EDA
Distribution of median housing prices for the top 25 zipcodes.
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/DistributionOfHousingPrices.png" width="500">

Looking at the raw data for 5 random zipcodes within the top 25 zipcodes.
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FiveRandomZipcodes.png" width="500">

We can see that Idaho housing market was also affected by the 2008 crash. Because of this we will start our modeling from 2011 so that the crash does not affect our model.

This is a map of the top 25 zipcodes. It is important to note that the color values for the latest historic 5 year ROI has changed since the previous map.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/25BestROIMap.png" width="500">



## Top 5 zipcodes
### Zipcode 83858

The graph below shows how the trained model did when predicting the test data. The test data was 6 months and we can see that initially the model did well at predicting the first couple months but failed to predict the sudden increase. Even though it was not able to predict the sudden increase the test values stayed within the 95% confidence interval shown within the green shaded area. The RMSE for this test prediction was $3,602.40

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/TestPrediction83858.png" width="500">

The graph below shows the final model and the predicted one year values based off of the current data we have. The output below the graph shows the price predicted and the low/high predictions for the 95% confidence interval. Using these values the 1 year ROI as well as the low/high 1 year ROI was calculated.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FinalModel83858.png" width="500">
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/83858Results.png" width="500">



### Zipcode 83605

The graph below shows how the trained model did when predicting the test data. The test data was 6 months and we can see that the model was able to predict the price fairly well. The RMSE for this test prediction was $1,330.62

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/TestPrediction83605.png" width="500">

The graph below shows the final model and the predicted one year values based off of the current data we have. The output below the graph shows the price predicted and the low/high predictions for the 95% confidence interval. Using these values the 1 year ROI as well as the low/high 1 year ROI was calculated.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FinalModel83605.png" width="500">
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/83605Results.png" width="500">


### Zipcode 83350

The graph below shows how the trained model did when predicting the test data. The test data was 6 months and we can see that the model was able to predict the price fairly well. The RMSE for this test prediction was $677.70

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/TestPrediction83350.png" width="500">

The graph below shows the final model and the predicted one year values based off of the current data we have. The output below the graph shows the price predicted and the low/high predictions for the 95% confidence interval. Using these values the 1 year ROI as well as the low/high 1 year ROI was calculated.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FinalModel83350.png" width="500">
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/83350Results.png" width="500">


### Zipcode 83845

The graph below shows how the trained model did when predicting the test data. The test data was 6 months and we can see that the model started the prediction right when the prices were declining and the model started to predict higher values than the true values. The predicted values and real test values seem to re-converge towards the end of the 6 month prediction. Even though it was not able to predict the sudden drop in price the test values stayed within the 95% confidence interval shown within the green shaded area. The RMSE for this test prediction was $5,944.20

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/TestPrediction83845.png" width="500">

The graph below shows the final model and the predicted one year values based off of the current data we have. The output below the graph shows the price predicted and the low/high predictions for the 95% confidence interval. Using these values the 1 year ROI as well as the low/high 1 year ROI was calculated.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FinalModel83845.png" width="500">
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/83845Results.png" width="500">


### Zipcode 83347

The graph below shows how the trained model did when predicting the test data. The test data was 6 months and we can see that initially the model started the predictions right when the prices took a sharp decline. The model was not able to predict this drop in price and the real values actually came out of the 95% confidence interval that is shown by the green shade. The real values and the predicted values do start to get closer towards the end of the 6 month prediction. The RMSE for this test prediction was $4,092.51

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/TestPrediction83347.png" width="500">

The graph below shows the final model and the predicted one year values based off of the current data we have. The output below the graph shows the price predicted and the low/high predictions for the 95% confidence interval. Using these values the 1 year ROI as well as the low/high 1 year ROI was calculated.

<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/FinalModel83347.png" width="500">
<img src="https://github.com/stevenkyle2013/ZillowTimeSeries/blob/main/Pictures/83347Results.png" width="500">


## Conclusion
Out of the 110 zipcoes that we have data on the best zipcodes to invest in are: 83858, 83605, 83350, 83845, and 83347. The predicted 1 year ROI spans from 5.48%-19.23%. Investment in zipcode 83347 warrants caution since the low 1 year prediction shows that there is the possibility that we would lose money on the investment.

## Recommendation
- Smaller cities seem to be experiencing more growth in price
- Areas where the median housing price is less than 300,000 seem to have a better ROI
