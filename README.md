# Module 2: Pandas-challenge

## Table of Contents

* [About](#about)
* [Tools](#tools)
* [Key Steps](#key-steps)
* [Summary](#summary)
    * [Create Pandas DataFrame](#create-pandas-dataframe)
    * [District Summary](#district-summary-snapshot)
    * [Per School Summary](#per-school-summary)
    * [Top 5 Highest Performing Schools](#top-5-highest-performing-schools)
    * [Bottom 5 Performing Schools](#bottom-5-performing-schools)
    * [Math Scores by Grade](#math-scores-by-grade)
    * [Reading Scores by Grade](#reading-scores-by-grade)
    * [Scores by School Spending](#scores-by-school-spending)
    * [Scores by School Size](#scores-by-school-size)
    * [Scores by School Type](#scores-by-school-type)

## About

This project involves the aggregation of school and student data to reveal trends in school performance among 15 schools.

## Tools

* Jupyter Notebook
* Pandas
* Pathlib

## Key Steps

#### **Import Dependencies & Merge Pandas DataFrames**

We begin by importing the necessary dependencies and merging data from CSV files.

```python
# Dependencies and Setup
import pandas as pd
from pathlib import Path

# File to Load
school_data_df = Path("Resources/schools_complete.csv")
student_data_df = Path("Resources/students_complete.csv")

# Read School and Student Data File and store into Pandas DataFrames
school_data = pd.read_csv(school_data_df)
student_data = pd.read_csv(student_data_df)

# Combine the data into a single dataset.
school_df = pd.merge(student_data, school_data, how="left", on=["school_name", "school_name"])
school_df.head()

```

---------------------------------------------------

#### **Import Dependencies & Merge Pandas DataFrames**
Created a high-level snapshot of the district's key metrics in a DataFrame

<img src="images\DistrictSnapshot.png"alt= "snapshot">

---------------------------------------------------

#### **Per School Summary**
Created a DataFrame called per_school_summary with columns for School Type, Total Students, Total School Budget, Per Student Budget, Average Math Score, Average Reading Score, % Passing Math, % Passing Reading,% Overall Passing.

<img src="images\PerSchool.png"alt="Perschool">

---------------------------------------------------

#### **Top 5 Highest Performing Schools**
Created a DataFrame with the Top 5 Performing Schools.

<img src="images\HighestPerforming5.png"alt="Top5">

---------------------------------------------------

#### **Bottom 5 Performing Schools**
Created a DataFrame with the Bottom 5 Performing Schools
<img src="images\Bottom5.png"alt="bottom5">

---------------------------------------------------

#### **Math Scores by Grade**
Created a DataFrame for Math Scores by Grade.
<img src="images\MathByGrade.png"alt="mathG">

---------------------------------------------------

#### **Reading Scores by Grade**

Created a DataFrame for Reading Scores by Grade.
<img src="images\ReadingByGrade.png"alt="readingG">

---------------------------------------------------

#### **Scores by School Spending**
Created a DataFrame for Scores by School Spending.

<img src="images\ScoreSchoolSpending.png"alt="schoolSpening">

---------------------------------------------------

#### **Scores by School Size**
Created a DataFrame for Scores by School Size

<img src="images\SML.png"alt="lms">

---------------------------------------------------

#### **Scores by School Type**
Created a DataFrame for Scores by School Type

<img src="images\SchoolType.png"alt="schooltype">

---------------------------------------------------

# Summary
After collecting the raw data from the PyCity School District, I cleaned and manipulated the data to apply statistics to help identify how many schools and students were in the PyCity School District by merging the raw data into one data frame. The merged data frame highlighted the District Summary, School Summary, Highest and Lowest-Performing Schools by Passing Percentage, Math and Reading Scores by Grade Level, Scores by School Spending, and Scores by School Size and Type.  I have been able to interpret these data frames and highlight key areas to make the data more cohesive and comprehensible to present to the parties of interest. This analysis will help the PyCity School District to be less reactive with resources and more proactive with strategies to bolster the district’s overall performance and student success. The report will concisely identify trends, correlations, and a synopsis of the data to present to the School Board.
The District Summary gave a broad look into the district’s 15 school totals, student population of 39,170 and outlining the School District’s Total Budget of 24,649,428 dollars . The data frame also gave a snapshot of the school district’s 78.9 percent average math score, 81.8percent average reading score, and overall passing rate of 65.1 percent. The School Summary also identified the school names and school type. This data will be essential for developing tactical data frameworks and strategies in other analysis sections in this report.
The Highest and Lowest-Performing Schools by Percentages gave a more narrowed interpretation of the data. The data frame indicated a strong correlation between Charter School Types having higher overall passing percentages and lower per-student budget. With the Charter School Type Overall Passing Percentage ranging from 90.5 percent to 91.3 percent and per student budget ranging from 582 dollars to 638 dollars. Meanwhile, the District School Types had higher per-student budget ranging from 655 dollars to 637 dollars and lower overall passing rates ranging from 52.9percent to 53.3percent.
The Math and Reading by Grad Level data frame gave a rudimentary summary and would indicate that all Grade Levels had passing percentages throughout 9th, 10th, 11th, and 12th grade, with a very low variation with each school’s individual grade level scores.  To provide a more ironclad analysis, I suggest adding variables such as school type and/or student population per grade level to bolster more cohesive research of this data frame to help fuel a transformative strategy for allocating resources for student success in these fields.
The Scores by School Spending highlighted a key Spending Range Per Student metric, essential in identifying a deficit in return on investment on the total budget. The evident correlation is that the District School Types have a higher Spending Range Per Student and lower scores and percentages across the fields highlighted in this data frame. The Charter School Types hold a solid return on investment of their Total Budget, with a lower Spending Range Per Student, yet higher scores and percentages, corroborating the opposite effect with the District Type of School correlation. Another conclusion from this data set is that the highest Overall Passing Percentage came from the Spending Range of less than 585 dollars.
The Scores by School Size data frame grouped student population sizes into three categories, Small, Medium, and Large. This metric helped identify that scores are impacted by student population, with the most successful scores within the School District coming from the Charter School Type and the Small to Medium School Sizes with populations ranging from less than a thousand and up to two thousand student population. In contrast, the District School Types had lower overall Scores and a larger student population of two thousand to five thousand. A limitation to this data set would be if socioeconomics has any direct impact on school type, school Size, and overall passing Percentages.
In conclusion, the data collected would reflect that the Charter School Types within the PyCity School District has an overall better success rate across all highlighted metrics within the data frames. The variable of lower student population in the Charter School Types was an evident contributor to a lower budget per-student and had a direct effect on return of investment on allocated resources on higher average math and reading scores and an overall higher passing percentage. To improve the analysis and assist in deploying a more proactive analysis of this data would be to add class size population per school type and per classroom budget in each individual academic subject. This would help identify any overinvestments with allocated resources.
