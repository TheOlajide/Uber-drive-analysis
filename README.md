## Uber Drive Data Analysis

### Table of content
-	Project Overview
-	Data Source
-	Tools
-	Data cleaning and preparation
-	Exploratory data analysis
-	Data Analysis
-	Results and Findings
-	Limitation

### Project Overview
This data analysis aims to answer important questions as regards the manner at which commuters use uber for trips. Time of trip preference and location, purpose for which trip is taken, days and month where trips are taken the most.


### Data source

Uber Drive dataset: The dataset used for this analysis is the ‘My uber drives-2016.csv’ file downloaded from Kaggle, containing information about trips taken from different location, date&time. We seek to analyze and answer important questions pertaining to this dataset.

### Tools
-Excel – Data Cleaning
-PowerBi – Data Cleaning, Analysis and creating report


### Data cleaning and preparation:

The following tasks were performed:

1.Data loading in excel and inspection
2.Data loading into PowerBi
3. Column Profiling to know the condition of columns
4. Handling and Replacing missing values
5. Separating date and time into different columns.
4.Handling error values, removing white or trailing spaces and fixing incorrect column data types..


### Exploratory Data Analysis

Objective of EDA was to answer the following questions:

1. What is the total length of trip?
2. What is the Average length of trip?
3. ⁠Average number of ride per week or month.
4. ⁠percentage of business miles to personal miles.
5. ⁠What hour do most people take uber to their destination?
6. Check the purpose of trips taken.
7. ⁠Which of the days has the highest number of trips?
8. ⁠What are the number of trips for each day?
9. ⁠What are the number of trips in each month?
10. ⁠Where do people start boarding their trip from the most(starting point of most trip)? 

### Data analysis

-	Date and time columns were extracted from original table and separated into another table and linked to uber drive table in the semantic model using a key.
-	Month name, month number, days of week, weeks of the year were extracted from date column using the add column button on the ribbon tab
-	Hour column was extracted from the time column using the above process.
-	Measures were created using DAX, to calculate the Average monthly and Average weekly trip.

```
Average monthly trip = Divide([Total trips], [Total months],0)

Total month = Distinct Count(Dates[Month Name])

Total trips = Countrows( my uber drives)
```
-	Other questions were answered using bar charts, doughnut and line chart.


### Results and Findings

From analysis of data, the following could be inferred;

1. Total length of trip is 12,205 in miles. This can also be referred to as the overall total miles travelled by all commuters.
2. ⁠Average length of trip is 10.576 in miles.
3. ⁠Average number of weekly ride is 21.76, while monthly ride is 96.25 in miles.
4. ⁠Percentage of business miles to personal miles is 93.33% to 6.67%
5. ⁠Most people take uber at 3pm. EDA shows the number of commuters is highest at 3pm noon.
6. ⁠EDA shows “others”(a missing value) as the major purpose of trips taken, having the highest record. Followed by other purposes like meeting, meal/entertainment, errands etc
7. ⁠The day with the highest number of trips is Friday, with a total of 206.
8. ⁠The number of trips for each day is represented on the chart below.
9. ⁠The number of trips in each month is represented on the chart below.
10. ⁠Most people start boarding their trip from a location called Cary. Conclusion and recommendation: It can be inferred that most commuters’ choice of time for trips is around 3pm noon, with 93% of miles travelled being for business purpose. Friday is the busiest of days and December the busiest month.


### Limitation

Missing Value: Missing values/cells were found on the “purpose(of trip)” column. It was however replaced as “others”, which represents the trips taken by commuters for “other” reasons. This value turned out to be the highest recorded purpose of trip followed by “meeting”.

