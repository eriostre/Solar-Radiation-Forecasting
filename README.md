# Solar-Radiation-Forecasting
This study compares three time-series forecasting paradigms—statistical, machine learning, and deep learning—using ten-years of historical weather data from Dublin. The objective is to evaluate the performance of Prophet, XGBoost, and LSTM when forecasting daily solar radiation under multiple preprocessing strategies. 

# Abstract
An extensive data analysis was conducted, including descriptive statistics, inferential testing, stationarity assessment, outlier detection, feature selection, and exploratory visualisation. These steps revealed strong annual seasonality, nonlinear feature relationships, and variability across meteorological variables, informing the modelling framework and feature-engineering decisions. Four experiments were conducted using cleaned data, differenced data, log-transformed data, and cross-validation. Results show that XGBoost achieved the highest overall accuracy, particularly with the cleaned and log-transformed datasets. Prophet delivered stable, and robust performance, ending in second place. LSTM underperformed relative to the other models, likely due to dataset size and short-term variability. The findings highlight that in data-restricted, highly seasonal environments, statistical and machine learning models outperform deep learning algorithms.


## Objectives
- Clean and preprocess time-series data
- Handle missing values and outliers
- Descriptive statistics
- Feature relationship
- Inferential statistics
- Train and compare Prophet, XGBoost, and LSTM models

## Experimental desing for evaluation

- Experiment 1: Baseline models with clean dataset
In the first experiment, all three models were developed and fine-tuned using the dataset obtained after Exploratory Data Analysis (EDA) and cleaning. No transformations were applied to the target variable (solar radiation).

- Experiment 2: Differenced target variable
The second experiment evaluates how differencing the target feature affects model performance.
First-order differencing was applied to solar radiation to remove long-term trends and reduce non-stationarity.

- Experiment 3: Log-transformed target variable
The third experiment investigates the effects of stabilising variance through a log transformation. Each model was trained on the log-transformed target and results were later inverted for evaluation.

- Experiment 4: Cross-validation using clean dataset
Cross-validation was used as an experimental procedure during model training. The evaluation consisted of computing the average of statistical performance metrics across all validation folds for the forecasting task.

- Experiment 5: 30-day forecasting ahead
Following the evaluation of Prophet, XGBoost, and LSTM models, the most accurate forecasting framework was selected based on the results of Experiments 1 to 4. These final architectures were then retrained using the full ten-year dataset, enabling each model to exploit all available information before generating the short-term forecast.

#
Overall, this research provides a comparative framework for solar radiation forecasting in data-constrained environments and contributes to the broader understanding of how different modelling paradigms behave under varying preprocessing strategies. The results offer practical utility for future time-series forecasting research.
