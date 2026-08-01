# Week 5 – Building a Baseline Model (Part 2 of 2)

## Overview

Week 6 continues the assessment of the clinical dataset by developing baseline models to predict Emergency Severity Index (ESI) levels. Logistic regression and a decision tree were trained and compared with a stratified random baseline. Their performance was evaluated using accuracy, per-class precision, recall and F1 scores, macro and weighted F1, and confusion matrices.

The analysis focused particularly on ESI Level 1 because these patients require immediate life-saving intervention and were summarised in a short report. 

---

## Learning Objectives

Week 6 focused and developing and evaluating reproducible baseline models through: 

- Preparing the triage features and ESI target for modelling
- Dividing the dataset using a reproducible train-test split
- Training logistic regression and decision tree classifiers
- Comparing both models with a stratified random baseline
- Evaluating performance across all five ESI levels
- Selecting and clinically justifying an appropriate primary metric
- Examining model errors and their potential consequences for patients
- Communicating the results to a clinical audience 

## Deliverables 
[Week 6 Notebook](../../Notebooks/Week6_Baseline_Model.ipynb) 
[Baseline Model Report](../../Docs/Week-6/baseline-report.pdf) 

Model Visualisations
- [Logistic Regression Confusion Matrix](../../Docs/Week-6/Figs/w6_confusion_logreg.png)
- [Decision Tree Confusion Matrix](../../Docs/Week-6/Figs/w6_confusion_tree.png)

## Model Evaluation 

The dataset was divided using an 80/20 stratified train-test split preserving the proportion of each ESI level in the training and test sets. A fixed random seed of 42 was used for the split and model training so that the results can be reproduced by another reviewer. Three models were compared in this assessment: 

- Stratified Random Baseline - Generated predictions according to the existing distribution of ESI levels
- Logistic Regression - Prodivded an interpretable baseline for predicting all five ESI levels
- Decision Tree - Used rule-based splits with a maximum depth of five

The models were evaluated using the following metrics: 
- Accuracy
- Precision
- Macro F1
- Weighted F1
- Recall 
- Confusion matrices

ESI Level 1 recall was selected as the primary clinical metric because it measures the proportion of highest-urgency patients correctly identified. Missing a Level 1 patient could delay immediate assessment and life-saving treatment. Accuracy alone was insufficient because the dataset was imbalanced and was dominated by the more common ESI Levels 2 and 3.

## Key Activities 

- Selected variables available during triage and excluded post-triage information to reduce data leakage risk
- Created a reproducible 80/20 stratified train-test split
- Trained a stratified random baseline, logistic regression and bounded-depth decision tree
- Calculated per-class and overall evaluation metrics
- Produced confusion matrices for both trained models
- Compared macro and weighted F1 scores.
- Examined errors involving critical ESI Level 1 patients
- Summarised the findings in a three-page clinical report.


## Key Findings
Logistic regression was the strongest baseline model, outperforming the decision tree and stratified random baseline across accuracy, macro F1 and ESI Level 1 recall. It produced predictions across all five ESI levels, while the decision tree predicted only Levels 2 and 3. However, logistic regression missed 12 of the 16 ESI Level 1 patients and correctly identified only 11.1% of Level 5 patients. The most clinically concerning errors involved Level 1 patients because assigning them a lower urgency could delay immediate life-saving care. Logistic regression is therefore recommended for further development but is not suitable for independent clinical deployment. Future work should address class imbalance, improve recognition of rare ESI levels, evaluate performance across demographic groups and retain clinician oversight.


