# Temperature Trends for Proposed Oahu Surf Shop

## Project Overview
The purpose of this project is to analyze Hawaii for a hypothetical client seeking to open a surf shop. Specifically, the temperature trends during the months of June and December are analyzed so that the client can make a more informed decision.

## Resources and Software

- Starting File: [hawaii.sqlite](https://github.com/jinwei1207/surfs_up/blob/main/hawaii.sqlite)
- Python 3.9.12
- psycopg2-binary 2.8.6
- SQLAlchemy 1.4.1

## Results

- The average temperature in Oahu during December is only 3.9°F cooler than June.
- The lowest temperature in December is 8°F colder than the lowest temperature in June.
- There are 10.7% less data points in December than June.
- There are more temperature measures in June at 1700 while only 1517 in December 

Below is a statistical summary for the month of June:  
![image](https://user-images.githubusercontent.com/104603177/177672194-8da3f526-fa65-4188-b89e-e6424c55ebd4.png)

Below is a statistical summary for the month of December:  
![image](https://user-images.githubusercontent.com/104603177/177672390-31924089-da6b-47c4-95d9-a36eb8e0beb6.png))

## Summary

Based on the analysis report above, Surf shop in Oahu will have less customers in December than in June due to the slight decrease in average daily temperature.

It is important to have the most relevant results when conducting analysis on a potential business venture. We are using two addtional queries to perform to gather more weather date for June and December which is most representive data during the selected year.
Dec_results = []
Dec_results = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 6).all()
Dec_results = []
Dec_results = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 12).all()









