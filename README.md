## Uber Drive Data Analysis

![uber dashboard](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/d48424e1-17bc-4440-bbb4-463a4517ce2f)


### Table of content
-	[Project Overview](#project-overview)
-	[Data Source](#data-source)
-	[Tools](#tools)
-	[Data cleaning and preparation](#data-cleaning-and-preparation)
-	[Exploratory data analysis](#exploratory-data-analysis)
-	[Data Analysis](#data-analysis)
-	[Results and Findings](#results-and-findings)
-	[Limitation](#limitation)

### Project Overview
This data analysis aims to answer important questions as regards the manner at which commuters use uber for trips. Time of trip preference and location, purpose for which trip is taken, days and month where trips are taken the most.


### Data Source

Uber Drive dataset: The dataset used for this analysis is the ‘My uber drives-2016.csv’ file downloaded from Kaggle, containing information about trips taken from different location, date&time. We seek to analyze and answer important questions pertaining to this dataset.

### Tools
- Excel – Data Cleaning

- PowerBi – Data Cleaning, Analysis and creating report


### Data cleaning and preparation:

The following tasks were performed:

1. Data loading in excel and inspection
2. Data loading into PowerBi
3. Column Profiling to know the condition of columns
4. Handling and Replacing missing values
5. Separating date and time into different columns.
4.Handling error values, removing white or trailing spaces and fixing incorrect column data types..

![power query](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/16f8716e-8825-40fb-b3d8-e567c8258c72)


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

![uber semantic models](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/d7725453-8444-4a30-81e8-87c412ac82fc)

-	Month name, month number, days of week, weeks of the year were extracted from date column using the add column button on the ribbon tab

![date table](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/6a162f3c-d719-4a10-a8d4-0f2a52087a60)

-	Hour column was extracted from the time column using the above process.

![time table](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/18cd556c-c31f-44b1-ad4f-55fc26f06e81)

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

![total miles travelled](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/ec94087d-9445-4b9b-981d-f9cafce93782)

2. ⁠Average length of trip is 10.576 in miles.

![avg of miles](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/b9d4887a-c655-4366-988b-ade5ee80e79a)

3. ⁠Average number of weekly ride is 21.76, while monthly ride is 96.25 in miles.

![avg weekly trips](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/91d400b1-8417-4e07-95f2-4d00a82538b2)

![avg monthly trips](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/b8d7deea-06fc-4a53-bf04-b28f4db0b8d7)

4. ⁠Percentage of business miles to personal miles is 93.33% to 6.67%

![% of business miles to personal](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/5c818a06-eb6f-4750-b1bb-4bd22570df23)

5. ⁠Most people take uber at 3pm. EDA shows the number of commuters is highest at 3pm noon.

![hour of trip commencement](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/e260d076-e8b8-47be-9652-dd1bd983b465)

6. ⁠EDA shows “others”(a missing value) as the major purpose of trips taken, having the highest record. Followed by other purposes like meeting, meal/entertainment, errands etc

![purpose of trip](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/bbb030e2-7542-49d3-8ec8-361226486e05)

7. ⁠The day with the highest number of trips is Friday, with a total of 206.

![days of the week by number of trips](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/b78215c8-39f8-4bde-aaa3-0a8e60f428cd)

8. ⁠The number of trips for each day is represented on the chart below.

![days of the week by number of trips](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/9dc74091-7529-427d-b683-94be3488686e)


9. ⁠The number of trips in each month is represented on the chart below.

![month by number of trips](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/0e814be4-e951-4cf1-ada3-3337a4162cc4)

10. ⁠Most people start boarding their trip from a location called Cary. Conclusion and recommendation: It can be inferred that most commuters’ choice of time for trips is around 3pm noon, with 93% of miles travelled being for business purpose. Friday is the busiest of days and December the busiest month.

![where people start boarding from the most](https://github.com/TheOlajide/Uber-drive-analysis/assets/155437593/b85e5672-0cbf-4728-aa52-b3309986355f)


### Limitation

Missing Value: Missing values/cells were found on the “purpose(of trip)” column. It was however replaced as “others”, which represents the trips taken by commuters for “other” reasons. This value turned out to be the highest recorded purpose of trip followed by “meeting”.

