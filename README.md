# Uni- and multivariate time series modeling with seasonal ARIMA, Prophet and deep learning for PM10 level in Cracow, Poland

In a project I downloaded air pollution data avaiable at [Environmental Protection Inspectorate's](http://powietrze.gios.gov.pl/pjp/archives#) website, sampled every day from January 2001 to December 2018 at different measurement stations in Poland. For modelling I chose PM10 measured in Cracow, particle pollutant with a diameter of 10 micrometres or less, one of the main smog's component. I preprocessed and trasformed data to python DataFrame, made exploratory analysis and feature engineering. Next step was bulding different time-series models and using them to forecast next's year PM10 level - models were trained up to June of 2018, remaining 6 months of 2018 were used for testing. The next stage was getting historical weather data to incorporate exogenous variables and run multivariate modeling. It was scraped from the [Polish Meteorolgical Institite](https://danepubliczne.imgw.pl/). To compare results I used RMSE metrics. 

## Motivation 

Deteriorating air quality is a real threat for everyone's health. I lived 5 years in Cracow where I did feel difference a smog can make in general well-being. I wanted to figure out what's the trend at different scales, are there any reccuring patterns, at what time it's better to stay home, what can one expect in the upcoming years? Time series might come in handy to aswer these and other questions. 

## Tools and pipeline 

I used the following pipeline:

1.	Download zip files for years 2001-2018 from [link](http://powietrze.gios.gov.pl/pjp/archives#) and extract excel workbooks
2.	Extract, transform and load PM10 data into python DataFrame
3.	Explonatory Data Analysis, Feature Engineering
4.	Build and analyse seasonal ARIMA model
5.	Build and analyse Prophet model
6.  Get weather data and choose exogenous variables from [link](https://danepubliczne.imgw.pl/)
7.  Build multivariate seasonal ARIMA and Prophet
8.	Build and analyse LSTM and GRU models (in progress)
9.	Performance analysis, conslusions and lessons learned

## Prerequisites

The project was done with [Python 3.7.4](https://www.python.org/downloads/release/python-374/) and the following libraries:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [Matplotlib](http://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [fbprophet](https://pypi.org/project/fbprophet/)
- [statsmodels](https://pypi.org/project/statsmodels/)
- [tensorflow](https://pypi.org/project/tensorflow/)
- [missingno](https://pypi.org/project/missingno/)

## Code

Code provided in `Timeseries_PM10.ipynb`
