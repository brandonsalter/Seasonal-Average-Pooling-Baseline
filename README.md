# Seasonal-Average-Pooling-Baseline

A composite time-series forecasting model that repeatedly fits on residual values of the previous round, using different pooled averages of date-time features for prediction values in each round. Final predictions are the combined predictions of all previous rounds. As such, the difference in trend following the training phase will not be accomodated during prediction.

I am grateful to my advisor, Dr. Bryan Bischof, who introduced this idea to me during an analytics practicum. Here is a link to his presentation at ODSC West 2021, where the model is discussed within the larger context of composition in ml: https://www.youtube.com/watch?v=6s7sNydlFks

The data was originally retrieved from ENTSO-E Transparency Platform, which provides access to electricity generation, transportation, and consumption data for the pan-European market.

I'm using German consumption data ranging from Jan 2015 to Jan 2020. The German load data was initially obtained with 15-min resolution. It has been resampled it on an daily basis for this analysis. The data was collated by Francois Raucent and posted on his Kaggle page linked below. The initial data preparation also closely resembles the method used in his accompanying notebook.

https://www.kaggle.com/datasets/francoisraucent/western-europe-power-consumption?select=de.csv
