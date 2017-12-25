## Abstract
This project uses the United States Unemployment Rate and the full text of the State of the Union Address between 1989 and 2017. It examines if the trend of the job topic in the State of the Union Addresses correlates with that of the unemployment rate over time. The trend of the count of the words “job” or “jobs” in the addresses and that of the unemployment rate were compared. It was found out that the two trends are correlated. When the unemployment rate becomes high, job is talked about more in the State of the Union Address. 

## Motivation
One of the uses of Natural Language Processing (NLP) is to gain insights from text. This research aims to find out if we can learn about the economic conditions from analyzing the political speeches. This can be helpful for historians to study the world in a particular time by analyzing large amount of text data of that period.

## Datasets
* United States Unemployment Rate between 1989 and 2017  https://data.bls.gov
* Full text of the State of the Union addresses between 1989 and 2017 https://www.kaggle.com/rtatman/state-of-the-union-corpus-1989-2017

## Data Preparation and Cleaning
Full text of the State of the Union Addresses
Texts were tokenized into lists of words for counting words. A function was defined to count words in text.
A Pandas DataFrame was made using “Year” as Index and the count of job words as a column.

Unemployment Rate data
The Excel downloaded was made into a CSV file. 
A Pandas DataFrame was made from the CSV file.
A column for annual average was added to the DataFrame by calculating the mean of the monthly values of each year.
The “Year” column was made the Index of the DataFrame 

Two DataFrames were merged into one on index for the final visualization.

## Method
Two words “job” and “jobs” are defined as related to the job topic.
These two words are counted in each year’s State of the Union Address. The trend is then visualized through a plot for easier observation. The study focuses on the trend – the rise and fall over time.
The average unemployment rate of each year is calculated by finding the mean of the monthly values. The yearly unemployment rate is then also plotted to show the trend, which is compared with that of the job word count in the addresses. 
The two trends are placed on the same plot for a closer observation where the findings are derived. The focus is to see whether the two trends correlate with each other.

## Acknoledgements
Source of datasets: 
* kaggle.com
* Bureau of Labor Statistics website

I learned how to generate World Cloud from Andreas Mueller’s Github Repository: https://github.com/amueller/word_cloud
