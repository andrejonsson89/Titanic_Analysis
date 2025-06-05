# Titanic_Analysis
I go over some interesting facts in the Titanic Dataset

I followed the [Data Science Hive](https://www.datasciencehive.com/data-analyst-path) website's [Homework 1.3](https://docs.google.com/document/d/1HN-zwCLdtYvAd3qWYxuD9TOikR1M_IUOtvLZ2lzW5lU/edit?tab=t.0#heading=h.rsgtiadapi5j) questions involving the [Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset).

## Part 1: Data Cleaning

### 1. Remove Duplicates
  I imported the table into Power Query (891 rows).<br/>
  I removed duplicate rows (but still 891 rows).<br/>
  So I deleted these steps since unnecessary.<br/>
  (This can also be seen in the Name column (891 distinct, 891 unique)).

 ### 2. Handle missing data
 Check for missing values in Age, Fare, or other columns.
 
 Close & Load Power Query to a PivotTable.<br/>
 Drag each column to the values field to see a count.<br/>
 Can conditional format to highlight cells with values not equal to 891.<br/>
 We can see that only the Age column has omitted values.

 ![1 - Missing Values](https://github.com/user-attachments/assets/ab81bb37-84e6-4405-b01e-da9c34f6e456)

 ## Part 2: Descriptive Statistics

### 1. Basic Calculations
Calculate the mean, median, and standard deviation for Age and Fare.

Can use the Excel functions for the table but I wanted to practice using the PivotTable functions.<br/>
Implicit measures = drag Age to values -> change to average<br/>
Doesn't work with Median.<br/>
Explicit measures = RC dataset -> add measure

![2 - Basic Statistics](https://github.com/user-attachments/assets/7178065a-e4b4-4864-b732-41efbcbb6deb)

### 3. Survival Analysis
Calculate survival rate and group by Sex and Pclass

Survivors Count = SUM([Survived]) = 342<br/>
Survival Rate = DIVIDE([Survivors Count],COUNTA([PassengerId])) = 38%

![3 - Survival Rate](https://github.com/user-attachments/assets/e4812fa7-c7e4-42ba-a97b-406a08457ad5)

Depending on what's most interesting, Rows and Pclass can be sorted accordingly for subtotal percentages.

![4 - Survival Analysis](https://github.com/user-attachments/assets/e80a7b9d-e06f-4363-9412-c5c9b0f1a158)

## Part 3: Data Visualization

### 1. Histogram
Create a histogram for Age to visualize the distribution of passenger ages.

insert tab -> pivotchart -> from this workbook's Data Model<br/>
first the calculations made pretty<br/>
then a histogram with age for each person

![5a - Histogram](https://github.com/user-attachments/assets/65594386-8d86-4946-b76c-26a2f523d8cf)

![5b - Histogram](https://github.com/user-attachments/assets/5b0ddbba-a08f-4e0a-a90a-56b6d4e59c80)

### 2. Bar Chart
Create a bar chart showing survival rates by Pclass

drag Pclass to rows and Survival Rate to values

![6 - Bar Chart](https://github.com/user-attachments/assets/5727ef1c-9b90-4758-a9a5-492df90e6561)

### 3. Pie Chart
Create a pie chart of passenger distribution by Sex

drag Sex to rows and to values<br/>
could have been interesting to display % instead of count in chart (especially since it's already in the table next to it)

![7 - Pie Chart](https://github.com/user-attachments/assets/2b71eaa9-c852-4295-85b1-4413a630db41)

## Part 4: Advanced Analysis

### 1. Conditional Formatting:
Highlight passengers who paid a fare higher than 75.

drag Name to rows and Fare to values<br/>
With conditional formatting: easy<br/>
With PivotTable: filter arrow value >75

![8 - Big Spenders](https://github.com/user-attachments/assets/1f730471-4603-4b67-ae7a-34ee51d69ba5)

### 2. Top 10 Analysis
Identify the 10 passengers who paid the highest fare.

With SORT() function = SORT(A2:B892,2,-1)<br/>
With PivotTable: filter arrow value top 10

![9 - Top 10](https://github.com/user-attachments/assets/e8fb61fb-bddb-4c48-ad45-0efc5c094ee7)

## Reflection Questions

### 1. What is the average and median age of passengers?
We can see the answer in the Basic Statistics sheet<br/>
but if we want to visualize the age distribution, we could approximate a bell curve.

![RQ - 1](https://github.com/user-attachments/assets/7f657c99-55c4-4800-9dfa-1ecb791d6c51)

### 2. Which Pclass had the highest survival rate?
This is exactly what we did in our Bar Chart sheet<br/>
but let's try to create a better visualization.

![RQ - 2](https://github.com/user-attachments/assets/b31d38a2-c20b-48de-a20f-5fb382060879)

### 3. Are younger passengers more likely to survive?
There doesn't seem to be much correlation in our scatter plot<br/>
but if we had to add a linear trendline, we can see that the answer is "only slightly".

![RQ - 3](https://github.com/user-attachments/assets/4ef18473-012c-4910-a1c0-0a5e2cbd8800)



If I would redo this whole thing:<br/>
Probably group together sheets so I wouldn't have this many.<br/>
"Missing Values" and "Basic Statistics" could just be "Statistics".<br/>
"Survival Rate" and "Survival Analysis" could just be "Survival".<br/>
"Histogram" and "Bar Chart" and "Pie Chart" could just be "Charts".<br/>
"Big Spenders" and "Top 10" could just be "Top Spenders".


