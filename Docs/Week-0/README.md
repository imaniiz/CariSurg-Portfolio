# Week 0 - Orientation, Onboarding & Python Readiness 

## Overview 
Week 0 served as an introduction to the CariSurg MedTech Pathways Healthcare AI Programme and focused on developing the foundational technical and clinical skills required for subsequent weeks. The week introduced both technical excersizes and the role of clinical AI within healthcare, responsible AI use and the importance of understanding clinical data before developing a machine learning model. 

## Learning Objectives
Week 0 focuses on onboarding into Clinical AI & Innovation workflow through:
- Data cleaning and exploratary data analysis
- Visualization of Mercer General Hospital emergency department triage data
- Interpretation of clinical vital signs
- Basic at-risk patient identification using rule-based logic
- Establishing a GitHub portfolio to document progression of the project

## Deliverables 
## Assignment 1 - Gender Column Data Cleaning 
Used introductory data cleaning techniques to standardise inconsistent gender values within the dataset by identifying variations in formatting and converting them into a consistent representation suitable for analysis.

[Assignment 1 Notebook](../../Notebooks/Assignment1_GenderColumnCleaning.ipynb)

## Assignment 2 - FiO2 Column Data Cleaning 
Worked as part of a group to clean the FiO₂ column of the patient dataset by identifying implausible values, handling missing data, and applying appropriate preprocessing techniques to improve data quality prior to analysis.

[Assignment 2 Notebook](Notebooks/Assignment2_DataCleaning_Fio2Column_Group.ipynb)

## Assignment 3 - Exploratory Data Analysis
Performed introductory exploratory data analysis on the emergency department dataset using Python. This included generating descriptive statistics, investigating missing values, and producing visualisations to better understand the distribution of key clinical variables.

[Assignment 3 Notebook](Notebooks/Assignment3_DataVisualization.ipynb) 

## Assignment 4 - Clinical Vital Sign Description 
For Assignment 4, we were required to select one vital sign from the emergency department dataset and write a short clinical overview discussing:

- What the vital sign measures
- Its normal clinical range
- Additional medical significance
- How it is used during triaging in emergency care

The available vital signs included:

- Age
- GCS (Glasgow Coma Scale)
- SBP (Systolic Blood Pressure)
- DBP (Diastolic Blood Pressure)
- MAP (Mean Arterial Pressure)
- Pulse
- Temperature
- Respiratory Rate (RR)
- FiO₂
- Gender

I selected the Glasgow Coma Scale (GCS) and explored its importance in assessing a patient’s level of consciousness and neurological condition during emergency triage.

[Assignment 4 Document](Docs/Week-0/Assignment4_VitalSignDescription.pdf)

## Assignment 5 - Unconsidered Clinical Metric
For Assignment 5, we were required to select a vital sign that was not included in the original emergency department dataset and write a short clinical overview discussing:

- What the vital sign measures
- Its normal clinical range
- Additional medical significance
- How it is used during triaging in emergency care

For this assignment, I selected Capillary Refill Time (CRT) and explored its role in assessing blood circulation and detecting signs of shock or cardiovascular instability in emergency patients.

[Assignment 5 Document](Docs/Week-0/Assignment5_UnconsideredMetrics.pdf)

## Assignment 6 - Triage Pseudocode
For the final Week 0 assignment, we were required to design a digital triaging model that could process patient data and categorize patients into risk levels. The model could be presented using pseudocode, flowcharts, instructions, or written explanations.

For my submission, I created a flowchart showing how a digital triage system can analyze patient vital signs such as GCS, blood pressure, pulse, respiratory rate, temperature, and FiO₂ to identify high-risk patients and assign appropriate triage categories based on clinical urgency. This assignment helped me better understand how healthcare AI systems can support emergency department decision-making.

[Assignment 6 Document](Docs/Week-0/Assignment6_TriagePseudocode.pdf)

## Skills Developed

Technical Skills 
- Python programming fundamentals
- Data cleaning using Pandas and visualisation using Matplotlib
- Exploratory data analysis 
- GitHub repository management

Clinical Knowledge 
- Emergency department triage workflows
- Interpretation of vital signs
- Rule based clinical decision making 


