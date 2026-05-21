# CariSurg Portfolio - Week 0 
## Overview
Welcome to my CariSurg MedTech Pathways portfolio repository. This repository documents my progress throughout week 0 of the Carisurg Healthcare AI Training Program as I develop skills in Python programming, healthcare data analysis and clinical AI within a Caribbean context. 

## Tools & Technologies
- Python
- Pandas
- Matplotlip
- Google Colab
- GitHub

## Assignments
This section contains my submissions, notes and notebooks completed throughout week 0 of the programme. 

## Assignment 1 - Data Cleaning (Gender Column)
This assignment focused on setting up the development environment and performing introductory healthcare dataset cleaning using pandas. 

### Tasks Completed
- Environment setup include mounting Google Drive in Google Colab and importing libraries
- Loading emergency triage csv dataset into pandas DataFrame
- Explored and previewed dataset to view patient records
- Cleaned and standardized inconsistent Gender column values by mapping gender entries to numerical values
  
[Assignment 1 Notebook](Assignment1_GenderColumnCleaning.ipynb)

## Assignment 2 - Data Cleaning (Fio2 Column)
This assignment is a continuation of assignment 1, focused on cleaning and preprocessing the introductory healthcare dataset cleaning, specifically the Fraction of Inspired Oxygen (FiO2) column. 

### Data Exploration 
The dataset was first inspected usinf df.info() and df.describe(). A missing or invalid value analysis was performed to identify clinically impossible measurements. The data was then visualised using a histogram and boxplot to observe outliers and abnormal distributions. 


### FiO2 Cleaning and Imputation Decisions
My group was assigned the FiO2 column representing the percentage of oxygen a patient is breathing. Normal atmoshpheric oxygen concentration is approximately 21%, while patients recieving ocygen therapy have higher FiO2 values. Clinically, FiO2 values should realistically remain between 21% and 100% 

Missing FiO2 values were replaced with the mode of the column which was determined to be 21%. The mode was used as opposed to the median or mean because it preserved a clinically realistic representative value for patients not receiving supplemental oxygen. 


### Tasks Completed 
- Inspected column datatypes and non-null counts
- Identified invalid healthcare values
- Converted clinically impossible values to NaN
- Cleaned object datatype columns and converted them to numeric formats
- Handled missing values using statistical imputation methods
- Used visualization techniques to inspect data before cleaning
- Evaluated healthcare measurements using real-world clinical reasoning

[Assignment 2 Notebook](Assignment1_GenderColumnCleaning.ipynb)

