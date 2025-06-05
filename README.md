# Titanic_Analysis
I go over some interesting facts in the Titanic Dataset

I followed the [Data Science Hive](https://www.datasciencehive.com/data-analyst-path) website's [Homework 1.3](https://docs.google.com/document/d/1HN-zwCLdtYvAd3qWYxuD9TOikR1M_IUOtvLZ2lzW5lU/edit?tab=t.0#heading=h.rsgtiadapi5j) questions involving the [Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset).

## Part 1: Data Cleaning

### 1. Remove Duplicates
  I imported the table into Power Query (891 rows).<br/>
  I removed duplicate rows (but still 891 rows).<br/>
  So I deleted these steps since unnecessary.<br/>
  (This can also be seen in the Name column (891 distinct, 891 unique)).<br/>

 ![1 - Missing Values](https://github.com/user-attachments/assets/ab81bb37-84e6-4405-b01e-da9c34f6e456)

 ### 2. Handle missing data
 Check for missing values in Age, Fare, or other columns.
 
 Close & Load Power Query to a PivotTable.<br/>
 Drag each column to the values field to see a count.<br/>
 Can conditional format to highlight cells with values not equal to 891.<br/>
 We can see that only the Age column has omitted values.<br/>

