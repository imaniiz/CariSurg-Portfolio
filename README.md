# CariSurg Portfolio - Week 0 
## Overview
Welcome to my CariSurg MedTech Pathways portfolio repository. This repository documents my progress throughout week 0 of the Carisurg Healthcare AI Training Program as I develop skills in Python programming, healthcare data analysis and clinical AI within a Caribbean context. 

Week 0 focuses on onboarding into Clinical AI & Innovation workflow through:
- Data cleaning and exploratary data analysis
- Visualization of Mercer General Hospital emergency department triage data
- Interpretation of clinical vital signs
- Basic at-risk patient identification using rule-based logic 

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

[Assignment 2 Notebook](Assignment2_DataCleaning_Fio2Column_Group.ipynb)

## Assignment 3 - Data Visualization 
This assignment focused on exploring healthcare data through visualization techniques using matplotlib. The goal was to use the raw emergency department pation data and develop meanigful visual representations that could support clinical decision making. 

### Visualization Planning 
Before visualization, the dataset variables were reviewed to identify clinically meanigfully relationships between patient vital signs and emergency care indicators. Clinical questions were developed in order to guide the selection of appropriate visualization types such as scatter plots, histograms and bar plots which were all explored during the tutorial. 


### Clinical Question 1: Do patients with higher body temperatures tend to have elevated heart rates?

A Heart Rate vs Temperature Scatter Plot was created to investigate the clinical question and clinical reference regions were added to improve interpretation: 

- Bradycardia threshold (<60 bpm)
- Tachycardia threshold (>100 bpm)
- Hypothermia region (<35°C)
- Fever/Prexia region (>37.5°C)

<img width="490" height="290" alt="Pulse vs Temp" src="https://github.com/user-attachments/assets/73ffee1f-0177-4445-9aba-3744c1f5eac7" />

### Clinical Question 2: How many patients require increased oxygen support compared to those who didn't?

A bar plot was created to visualize the distribution of oxygen support levels (FiO2) among emergency departmentment patients. Logarithmic scaling was explored to better visualize less common oxygen categories. The visualization categorised patients based on their FiO2 levels: 

- Room air/ No oxygen support (21%)
- Supplemental oxygen support levels (40% - 100%)

<img width="550" height="300" alt="Oxygen Support" src="https://github.com/user-attachments/assets/2bb85c16-5ca8-4025-84da-f39b9c2a6b79" />


### Tasks Completed 
- Explored healthcare variables and identified clinically meaningful relationships
- Selected appropriate visualization methods based on data types and clinical questions
- Created scatter plots and bar plots using matplotlib
- Added clinical threshold lines, shaded regions and annotations
- Used visualization techniques to support potentional clinical interpretation and decision making

[Assignment 3 Notebook](Assignment3_DataVisualization.ipynb) 



