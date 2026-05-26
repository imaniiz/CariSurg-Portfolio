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

## Assignment 4 - Vital Sign Description 

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

One of the primary vital signs used by healthcare professionals is the Glasgow Coma Scale (GCS). It is a neurological assessment tool used to determine and monitor the consciousness of patients by observing how they respond to basic instructions and stimuli. In the medical context, consciousness refers to how awake, alert and oriented a patient is. Healthcare providers perform GCS assessments by evaluating the patient in three categories: eye opening, motor response and verbal response. The verbal response is done by observing the patient’s response to certain questions to test their memory and awareness. The motor response involves applying pressure to areas such as the nail beds, trapezius muscle and supraorbital notch and observing the patient's reflexes and reactions. The eye response evaluates the patients ability to open their eyes. Each category is assigned a score of 1 to 6 and the combined total gives the overall GCS score, which has a clinical range of 3 to 15. A lower GCS score indicates severe impairment of consciousness. A score  of 3 to 8 indicates severe traumatic brain injury, 9 to 12 indicates moderate injury and 13 to 15 indicates mild injury. During triaging in the emergency department, healthcare professionals therefore prioritize patients with lower GCS scores because they are considered to be in more critical condition and are in greater need of immediate medical attention.

## Assignment 5 - Unconsidered Metrics 

For Assignment 5, we were required to select a vital sign that was not included in the original emergency department dataset and write a short clinical overview discussing:

- What the vital sign measures
- Its normal clinical range
- Additional medical significance
- How it is used during triaging in emergency care

For this assignment, I selected Capillary Refill Time (CRT) and explored its role in assessing blood circulation and detecting signs of shock or cardiovascular instability in emergency patients.

Capillary Refill Time (CRT) is another important vital sign that was not previously considered in the dataset. CRT is a clinical assessment used to detect changes in the patient’s blood circulation, in the arms and legs. When there is a sudden decrease in blood flow, a patient can go into shock meaning that their organs may not be receiving sufficient oxygen for proper functionality. A CRT assessment is therefore a quick and efficient method used to detect blood flow issues when a patient enters the emergency department. CRT assessments are typically performed when a patient is at risk of shock or becomes unstable due to symptoms such as loss of consciousness, altered mental state and rapid changes in body temperature. The assessment is performed by elevating one hand or foot above the heart, applying pressure to one finger or toe for up to 10 seconds and observing the time it takes for the skin to return to its original colour after the pressure is released. For a healthy person, the expected CRT would be 2 seconds or less in infants and around 3 seconds or less in adults. During training, an unusually long CRT in a patient may indicate poor blood circulation, shock or cardiovascular problems and they would be prioritised for immediate medical attention. 

## Assignment 6 - Triage Pseudocode

For the final Week 0 assignment, we were required to design a digital triaging model that could process patient data and categorize patients into risk levels. The model could be presented using pseudocode, flowcharts, instructions, or written explanations.

For my submission, I created a flowchart showing how a digital triage system can analyze patient vital signs such as GCS, blood pressure, pulse, respiratory rate, temperature, and FiO₂ to identify high-risk patients and assign appropriate triage categories based on clinical urgency. This assignment helped me better understand how healthcare AI systems can support emergency department decision-making.






