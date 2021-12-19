# Installation
Project is written in Python 3.8.0

It uses libraries which are available in an Anaconda distribution.
Those include :
* pandas
* numpy
* scikitlearn
* matplotlib
* seaborn

Apart from that a library shap (2.1.0) was used to analyse regression model feature importance.
It can be installed using ```pip install shap```

# Project Motivation
The projects looks into the AirBNB dataset from Boston.
I chose this dataset, as I undertsood the business context quite well and could immediately come up with some interesting questions to verify in the data.


# File Descriptions
All the data sources can be found in ./Data directory. They were downloaded from [kaggle] (https://www.kaggle.com/airbnb/boston?select=listings.csv)
[More information about the dataset] (http://insideairbnb.com/about.html)

There are 2 jupyter notebooks in the project:
* price_prediction: file where listings data set is analysed to understand what are the key features that impact listing price on AirBnB
* calendar_data_exploratio: file with dive into the calendar dataset and seasonality of demand on AirBNB in Boston


# How To Interact With Your Project 
The data prooved to be quite messy and a lot of volume of code is spent on data cleaning.

I had issues with interpretation of "availability_rate "calculated based on the calendar dataset. According to the documentation, the flag informing whether listing is available or not may mean that given apartment is booked, or it's marked as unavailable by the owner. This data had some suspicious spikes in the availabilitiy rate, that I could not explain easily.

In the price_prediction I go through a lengthy process of data cleaning and data extraction </br>
In the end I have random forest regression model, predicting the price of listings. Based on the model, feature importance was assessed, using Shapley values [docs](https://shap.readthedocs.io/en/latest/example_notebooks/overviews/An%20introduction%20to%20explainable%20AI%20with%20Shapley%20values.html)


# Licensing, Authors, Acknowledgements
I used a lot of on-line resources when looking for the best way to find answers to my q uestions.
One of the biggest sources of knowledge was https://machinelearningmastery.com/ website, where I looked for examples of one-hot encoding.
https://mljar.com/blog/feature-importance-in-random-forest/ was the tutorial I used to get Shapley values for the random forest model
