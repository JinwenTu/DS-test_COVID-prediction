# DS-test_COVID-prediction
COVID prediction

## Description
The White House Office of Science and Technology Policy (OSTP) pulled together a coalition research groups and companies (including Kaggle) to prepare the COVID-19 Open Research Dataset (CORD-19) to attempt to address key open scientific questions on COVID-19. Those questions are drawn from National Academies of Sciences, Engineering, and Medicine’s (NASEM) and the World Health Organization (WHO).

Kaggle is launching a companion COVID-19 forecasting challenges to help answer a subset of the NASEM/WHO questions. While the challenge involves developing quantile estimates intervals for confirmed cases and fatalities between May 12 and June 7 by region, the primary goal isn't only to produce accurate forecasts. It’s also to identify factors that appear to impact the transmission rate of COVID-19.

Using the train dataset from this Kaggle's COVID-19 forecasting series, I'm trying to predict the confirmed and fatal cases in different countries between 11th to 17th May based on the case numbers from Jan to 10th May. 

## Approach
### 1. Download the dataset:
There are columns in this dataset: Id, County, Province_State, Country_Region, Population, Weight, Date, Target and TargetValue. Missing values are existing in County and Province_State, but since I'm going to predict based on countries, they are left as missing. Negative values are existing in TargetValues, and based on the real world data, they have been converted to positive values.

### 2. Data visualization:
The COVID case trend over time was pulled out for top-10 countries in confirmed/ fatal case numbers. The daily increased cases in most countries were peaked in April and gradually decrease in May, except for Brazil and Russia.

### 3. Prediction:
Random Forest model was chose to make the prediction based on the data before 11th May. The accuracy looks good.
