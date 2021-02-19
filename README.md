# Gender and ethnic analysis in the accuracy of age estimation

## Description

This project is part of Digital Project Course in the Master of Digital Science in the Center for Research and Interdisciplinarity -CRI- Paris. France

The research aims to explore the existence of gender and ethnic bias in the accuracy of age estimation based on images. The dataset used in this analysis is from AgeGuess, a citizen science project on human biological and chronological age.  

* **Importance of Age Estimation** 

Age estimation is becoming more common nowadays; it is useful in different applications, such as video surveillance, demographics collections, business intelligence, recognition of people for business, social or humanitarian purposes; the scenarios are different. However, how the observer estimated the apparent age of a person needs a better comprehension of bias and the accuracy in age estimation because these datasets are using more and more for prediction based on Machine Learning algorithms. An inaccurate dataset may increase inequalities in society. 

* **AgeGuess** is an online game using biological and perceived age as biomarkers to address ageing humans' scientific questions. Trough gamification of the perceived age enables the collection of large amounts of data.

![logoAgeGuess](https://github.com/merlynjocol/AgeGuess-Data-Analysis--Gender-Ethnic-analysis-in-age-guessing/blob/main/logoAgeGuess.png)

https://www.ageguess.org/


## Table of Contents:

** Exploratory Data analysis
* Research questions
* Cleaning data & Featuring
* Visualizations 

** Data Analysis 
* Cleaning data & Featuring
* Merge databases
* Analysis 
* Visualizations

## Files in the respository
* AgeGuess EDA
* AgeGuess_Analysis
* Pitch presentation 
* Images of the results
* Dataset with GeoVariables: custom.geo.json


## Dataset information. 

* Public Data Set: https://www.ageguess.org/download

**Database information** 
* 220.231 Age guess  
* 4651 photos have been uploaded by citizens and used by gamers 
* 4437 citizens who have engaged with the project since 2012
* 3644 Gamers (guessers) 

**Variables**

**Database Gamers** 
* *(uid)* individual identifier of the user 
* *(g)* number of correct guesses the user made 
* *(ng)* number of other guesses 
* *(points)* points gained in the online game 
* *(gender)*, *(ethnicity)*, *(birth country)*, and *(birth year)* is users’ basic demographic information
* *(access)* date when the user last logged 
* *(created)*  date when the user created an account with AgeGuess. variables store the timestamp in date and time UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS’

**Database Guess**
* *(uid)* individual identifiers of the user who made the guess
* *(guess_id)* the guess itself
* *(photo_id)* the photograph guessed 
* *(ageG)* guessed age
* *(outG)* the deviation in the guess from the real age in years
* *(access)* date and time of the guess  UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS’

**Database Photos**
* *(uid)* individual identifier of the user who uploaded the photograph 
* *(photo_id)* Id for  the photograph uploaded.
* *(relation)* variable indicates whether the photograph is of the user or of another person to which the user has a relation (categories: user, unrelated of friend, mother/father, son/daughter, sibling, half sibling, maternal/paternal grandparent, maternal/paternal aunt/uncle, maternal/paternal cousin, grandchild). 
* *(gender)*,*( ethnicity)*, *(birth_country)*, *(birth_year)*, *(death_age)* variables contain the respective basic demographic information for the person in the photograph. 
* *(created)* variable stores the timestamp when the photograph was added in date and time UTC + 1:00 ‘YYYY-MM-DD HH:MM:SS’.

## Installation:
* Python 3.7
* The project were developed in DeepNote and Google drive

#Python libraries
* import pandas as pd
* from pandas import DataFrame, read_csv   #conda install -c anaconda xlrd
* from datetime import datetime
* import numpy as np
* import functools
* from functools import reduce

#graphs
* import os
* from plotly.offline import init_notebook_mode, iplot
* import plotly.graph_objs as go
* init_notebook_mode(connected=True)
* import matplotlib
* import matplotlib.pyplot as plt
* from matplotlib import rcParams
* from matplotlib import gridspec
* import seaborn as sns
* import functools
* from functools import reduce

#map graphs and geovariables
* import geopy
* import folium
* from folium.plugins import MarkerCluster

#build reports
* from pandas_profiling import ProfileReport


## Credits:
* AgeGuess Citizen Project to provide the databases. Online Game Access https://www.ageguess.org/home
* Dusan Misevic for giving feedback on the results. Researcher at CRI - Center for Research and Interdisciplinary, Paris, France 
* Master AIRE -CRI- Center for Research and Interdisciplinary, Paris, France 
* 
## License: Copyright Open


