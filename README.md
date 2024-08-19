# Patient Stay Prediction

This project predicts the length of stay for patients in a hospital-based
 on various features. 

## Installation

To run this project, you need to have Jupyter Notebook and the required Python libraries installed.

## Introduction
The goal is to build a model to predict the length of stay of a patient given the readings and history from when the patient was admitted. The project leverages machine learning models such as Linear Regression to predict this.

## EDA Findings

1. Identified key features influencing patient stay duration.
   
2. Discovered correlations between patient history and length of stay.
   
3. Highlighted potential outliers and missing data that may affect the model.


## Dataset
The dataset includes information on patient hospital stays, with 10,999 rows and 13 columns. After removing two columns with no values (KidneyAilments and HeartAilments), there are 11 independent features and one target variable, LengthOfStay. Independent features include categorical and boolean variables such as Gender, PsychologicalAilments, and SubstanceAbuseHistory.

## Data Preprocessing

Data preprocessing steps included:

•	Handling missing values

•	Removing duplicate entries

•	Converting categorical variables to numerical format using one-hot encoding

•	Normalizing numerical features

•	Splitting the data into training and test sets


## Feature Engineering

The dataset includes the following features:

•	LengthOfStay: Number of days a patient stays in the hospital (target variable).

•	Id: Unique patient identifier.

•	ReadmissionCount: Number of times the patient has been readmitted.

•	Gender: Patient's gender.

•	FacilityId: Facility identifier.

•	KidneyAilments: Presence of kidney ailments.

•	HeartAilments: Presence of heart ailments.

•	PsychologicalAilments: Presence of psychological ailments.

•	SubstanceAbuseHistory: History of substance abuse.

•	BMI: Body Mass Index.

•	ABG: Arterial blood gas levels.

•	Pulse: Pulse rate.

•	SecondaryDiagnosis: Secondary diagnosis code or category.

Due to outliers in BMI and Pulse, imputation was done using the mode instead of the mean. 
For SecondaryDiagnosis, the mode was used for imputation, as the most common value was 1.0. Mode and median calculations were performed on training data only to avoid data leakage when applied to test data.

## Model Training & Tunning 

The model was trained using 
•	Linear Regression

The model was tuned using
•	Ridge

•	Lasso

to see if there would be any significant change in its R2 score

## Usage

Open `Patient_Stay_Prediction.ipynb` in Jupyter Notebook to explore the analysis and prediction process.

## Requirements

- Python 3.x
- Jupyter Notebook
- pandas
- scikit-learn

