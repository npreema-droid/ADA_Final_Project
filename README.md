# ADA_Final_Project
Depression Diagnosis Predicting Diabetes
Nusrat Sharmin Preema
ID: 527349, MPH (Epidemiology and Biostatistics)
Advanced Data Analysis, Fall’25
Instructor: Kim Jhonson


# ADA Final Project: Depression and Diabetes Analysis Using NHANES publicly available data set 2021-2023

 Project Overview
This project was completed as part of the Applied Data Analysis (ADA) course.  
The objective was to evaluate whether depressive symptoms are associated with diabetes prevalence among U.S. adults using publicly available NHANES data.  
The analysis includes data cleaning, variable recoding, descriptive statistics, logistic regression modeling, and several stratified visualizations.


Repository Contents
 1. ADA_clean_analysis.R
This file contains all R code used to:
- Import NHANES data  
- Clean and recode variables  
- Create depression, diabetes, gender, race, and age group variables  
- Run logistic regression models  
- Generate bar plots stratified by age, sex, and race  
- Save the cleaned dataset  

 2. ADA_final_project.Rmd  
RMarkdown file that contains the narrative explanation, code chunks, statistical output, figures, and interpretations used for the final report.

3. ADA_clean.csv  
The cleaned NHANES analytic dataset used in the project.  
Includes the following variables:
- ‘SEQN’
- ‘diabetes’, ‘diabetes_f’  
- ‘depress01’, ‘depress_f’ 
- ‘gender’ 
- ‘race3’  
- ‘age’, ‘age_group’


This dataset is fully derived from the publicly available NHANES datasets 2021-2023.

 4. README.md 


#Research Question
Is depression associated with the odds of having diabetes among adults in NHANES during 2021-2023, after adjusting for age, sex, and race?



##  Methods Summary

#Data Source
National Health and Nutrition Examination Survey (NHANES), publicly available through the CDC.

Key Variables
- Depression: DPQ020 (re-coded to depress01, depress_f)
- Diabetes: DIQ010 (re-coded to diabetes, diabetes_f)
- Demographics:
  - age (continuous) -> age_group
  - gender (Male/Female)
  - race3 (White / Black / Other)

Statistical Analysis
- Descriptive statistics  
- Unadjusted logistic regression  
- Multivariable logistic regression (adjusted for age, sex, race)  
- Stratified bar plots:
  - by age group  
  - by gender  
  - by race  


Key Findings
•	Individuals with depressive symptoms had significantly higher odds of diabetes after adjusting for age, sex, and race
OR = 1.65, 95% CI: 1.39–1.97, p < 0.001
•	Age was strongly associated with diabetes; each year increased odds by 5%
•	Sex differences: Females had lower odds of diabetes compared to males
•	Race differences:
1.	Black adults had 2.46 times higher odds of diabetes than White adults
2.	Other-race adults also had significantly elevated odds
•	Bar charts showed consistent patterns: diabetes was higher in depressed individuals across all age, sex, and race groups


# R Packages
```r
library(dplyr)
library(ggplot2)
library(readr)
library(tidyr)

Author
Nusrat Sharmin Preema
MPH (Epidemiology & Biostatistics)
Washington University in St. Louis
Advanced Data Analysis – Fall 2025

Notes
•	All data used in this project are publicly available and contain no restricted or personally identifiable information.
•	This repository is intended for educational and reproducibility purposes.


