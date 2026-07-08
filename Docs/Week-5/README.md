# Week 5 – AI-Assisted Triage: Data Exploration (Part 1 of 2)

## Overview

Week 5 marked the transition from research and project planning to working with a real clinical dataset. This week's focus was evaluating the quality, completeness, and suitability of a de-identified emergency department dataset for developing an AI-assisted triage model. Throughout this week, I performed exploratory data analysis (EDA), investigated missing values and inconsistencies, examined the distribution of important clinical variables, and assessed potential predictors of patient triage level. The findings were summarised in a feasibility memo intended for a clinical audience, providing recommendations on whether the dataset was suitable for model development and highlighting important limitations that should be considered during subsequent modelling.

---

## Learning Objectives

Week 5 focused on applying data analysis techniques to evaluate the quality and feasibility of a real-world clinical dataset through:

- Exploring the structure and clinical context of a de-identified emergency department dataset.
- Identifying missing values, inconsistent data types, and potential outliers.
- Producing visualisations to assess data quality and feature distributions.
- Evaluating whether the dataset was suitable for machine learning applications.
- Identifying clinical variables that may be predictive of patient triage level.
- Communicating technical findings through a feasibility memo written for a clinical audience.

## Deliverables 
[Week 5 Notebook](../../Notebooks/Week5_Data_Exploration.ipynb) 
[Clinical Feasibility Memo](../../Docs/Week-5/data-feasibility-memo.pdf) 

Data Visualisations
- [Data Missingness Map](../../Docs/Week-5/Figs/figs-01-missingness.png)
- [ESI and Age Distribution](../../Docs/Week-5/Figs/figs-02-esi-age.png)
- [Demographic Distribution](../../Docs/Week-5/Figs/figs-03-missingness.png)
- [Chief Complaints Distribution](../../Docs/Week-5/Figs/figs-04-chief-complaints.png)
- [Vitals by ESI Boxplot](../../Docs/Week-5/Figs/figs-05-vitals-by-esi.png)
- [Vitals and ESI Correlation](../../Docs/Week-5/Figs/figs-06-correlation.png)
  


## Key Activities 

- Profiled a 55,121-patient emergency department dataset
- Organised variables into feature families
- Assessed dataset completeness using missingness tables and visualisations
- Verified clinical plausibility of vital signs using established physiological ranges
- Identified statistical outliers while distinguishing them from clinically plausible extreme observations
- Evalueted target class balance for ESI
- Explored relationships between vital signs, chief complaints and ESI
- Produced demogrpahic and equity visualisations to assess representation across patient groups
- Summarised findings and recommendations within a clinical feasibility memo

## Key Findings
The exploratory analysis found that the emergency department dataset is suitable for baseline AI-assisted triage modelling, with several important considerations. The structured clinical variables were complete and the recorded vital signs were clinically plausible, with no physiologically impossible observations. Exploratory analysis identified a noticeable class imabalnce in the ESI with Levels 2 and 3 representing the majority of patient encounters, indicating that future models should account for this during triaging and evaluation. Vital signs such as oxygen saturation and chief complaints such as cheif complaints showed meaningful correlation with higher acuity. Demographic and equity analyses did not reveal any obvious disparities across patient groups. However, fairness should continue to be monitored during model development. Overall, the findings support proceeding to baseline predictive modelling while recognising the limitations identified during the data quality assessment. 

