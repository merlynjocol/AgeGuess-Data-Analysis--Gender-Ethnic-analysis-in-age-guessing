# Gender and ethnic analysis in the accuracy of age estimation

# Description:

This project is part of Digital Project Course in the Master of Digital Science in the Center for Research and Interdisciplinarity -CRI- Paris. France

The research aims to explore the existence of gender and ethnic bias in the accuracy of age estimation based on images. The dataset used in this analysis is from AgeGuess, a citizen science project on human biological and chronological age.  

* **Importance of Age Estimation** 

Age estimation is becoming more common nowadays; it is useful in different applications, such as video surveillance, demographics collections, business intelligence, recognition of people for business, social or humanitarian purposes; the scenarios are different. However, how the observer estimated the apparent age of a person needs a better comprehension of bias and the accuracy in age estimation. Inaccuraty in age estimation may increase inequalities in society. 

* **AgeGuess** is an online game using biological and perceived age as biomarkers to address ageing humans' scientific questions. Trough gamification of the perceived age enables the collection of large amounts of data.

![logoAgeGuess](https://github.com/merlynjocol/AgeGuess-Data-Analysis--Gender-Ethnic-analysis-in-age-guessing/blob/main/logoAgeGuess.png)

https://www.ageguess.org/


# Approaching the Solution:

## 1 Exploratory Data analysis
* Research questions. After install and explore the data, I re-defined the research questions and the scope of the research. In the beginning,  I planned to analyzed the bias and accuracy in age estimation based on gender, ethnicity and country wellbeing, but the dataset has few ageestimationdata for guessers from low and middle-income countries; for that reason, this study does not include wellbeing indicators and is focus on gender and ethnicity. 
* Cleaning data & Featuring. Remove outliers fromm gamers who has year of birth before 1934. The country names in the dataset of gamers and photos need to change to the standard names used for Nature Earth, to connect with geovariables and build the maps. 
* Exploratory visualizations: The visualization are reports (pandas_profiling import ProfileReport), maps, piecharts, barplots, histograms and lineplots in every dataset

## 2 Data Analysis 
* Featuring: create new variables in the dataframes to do the analyses related to Accuracy (Mean Absolute Error - MAE)
* Merge databases: The datasets merged were ag_gamers, ag_guess and ag_photos
* Analysis: the analysis was base on the bias (real age - estimation age) and the Accuracy (absolute value of bias); the study takes the entire age estimation, and it is cross trough ethnicities and gender 
* Visualizations: barplots, scatterplots, heatmap

# Files in the respository
* AgeGuess EDA
* AgeGuess_Analysis
* Pitch presentation 
* Results image


# Installation guide:

**Code and Data**

* `notebook.ipynb` : Python code with libraries pandas, datetime, numpy, functools
* Build reports: ProfileReport, pandas_profiling 
* Graphs libraries:  matplotlib, pyplot, seaborn 
* Maps libraries: geopy, folium

**Datasets** 
* `ag_guess.csv` Dataset with 220.231 Age guess
* `ag_gamers.csv` Dataset of 4651 photos have been uploaded by citizens and used by gamers 
* `ag_photos.csv` Dataset of 4437 citizens who have engaged with the project since 2012
* `custom.geo.json`: Dataset with geovariables of the countries and worldmap. https://geojson-maps.ash.ms/
* Access to the Public AgueGuess Dataset: https://www.ageguess.org/download

**Variables information**

`ag_guess.csv` 
* *(uid)* individual identifier of the user 
* *(g)* number of correct guesses the user made 
* *(ng)* number of other guesses 
* *(points)* points gained in the online game 
* *(gender)*, *(ethnicity)*, *(birth country)*, and *(birth year)* is users’ basic demographic information
* *(access)* date when the user last logged 
* *(created)*  date when the user created an account with AgeGuess. variables store the timestamp in date and time UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS’

`ag_gamers.csv`
* *(uid)* individual identifiers of the user who made the guess
* *(guess_id)* the guess itself
* *(photo_id)* the photograph guessed 
* *(ageG)* guessed age
* *(outG)* the deviation in the guess from the real age in years
* *(access)* date and time of the guess  UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS’

`ag_photos.csv`
* *(uid)* individual identifier of the user who uploaded the photograph 
* *(photo_id)* Id for  the photograph uploaded.
* *(relation)* variable indicates whether the photograph is of the user or of another person to which the user has a relation (categories: user, unrelated of friend, mother/father, son/daughter, sibling, half sibling, maternal/paternal grandparent, maternal/paternal aunt/uncle, maternal/paternal cousin, grandchild). 
* *(gender)*,*( ethnicity)*, *(birth_country)*, *(birth_year)*, *(death_age)* variables contain the respective basic demographic information for the person in the photograph. 
* *(created)* variable stores the timestamp when the photograph was added in date and time UTC + 1:00 ‘YYYY-MM-DD HH:MM:SS’.


# Results:

![logoCRI](https://github.com/merlynjocol/AgeGuess-Data-Analysis--Gender-Ethnic-analysis-in-age-guessing/blob/main/Results_AgeEstimation.JPG)

# Credits:
* AgeGuess Citizen Project to provide the databases. Online Game Access https://www.ageguess.org/home
* Dusan Misevic for the feedback on the results. Director of Research Affairs at CRI - Center for Research and Interdisciplinary. Paris, France 
* Master AIRE -CRI- Center for Research and Interdisciplinary. Paris, France 

<img src="https://github.com/merlynjocol/AgeGuess-Data-Analysis--Gender-Ethnic-analysis-in-age-guessing/blob/main/logoCRI.jpg" width="100" height="100">

# License: 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



