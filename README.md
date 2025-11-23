📘 README – Heart Disease Prediction (KNN Model)

Project Overview

This project applies a K-Nearest Neighbors (KNN) machine learning model to predict Coronary Artery Disease (CAD) using key clinical indicators. The analysis is based on a medically validated dataset and aims to support early detection of heart disease through data-driven methods.

Dataset & Preprocessing

The dataset includes several clinical measurements such as age, sex, cholesterol levels, ST depression, exercise-induced angina, and fluoroscopy results.

Key preprocessing steps included:

Converting character variables (e.g., ca, thal) into numeric values

Creating a binary diagnosis column (1 = disease present, 0 = no disease)

Removing missing values using na.omit()

Selected Predictors

Five variables were chosen for the predictive model based on their strong clinical relevance:

Age

Sex

Exercise-Induced Angina (exang)

ST Depression (oldpeak)

Number of Major Vessels with Calcium (ca)
These variables have been consistently validated in medical literature as significant predictors of CAD.

Modeling Approach

A KNN classification model was trained to distinguish between healthy and diseased patients.
The model was tuned for optimal K-value performance and validated using accuracy and confusion-matrix evaluation.

Results

The model achieved:

High overall accuracy

90.1% accuracy when predicting no disease

76.9% accuracy when predicting presence of disease (36 of 109 illness cases were misclassified)

Interpretation

The model works very well for identifying patients without CAD.

Sensitivity for detecting actual disease cases is lower, suggesting the need for additional predictors or more advanced models.

Future Directions

The HTML report identifies several research extensions, including:

Improving sensitivity for severe CAD cases

Comparing KNN with more advanced ML algorithms

Conducting real-world clinical validation

Evaluating cost-effectiveness in healthcare settings

Conclusion

The KNN approach proves effective for general CAD prediction and demonstrates strong potential as a clinical decision-support tool. However, further refinement is required before applying it to high-risk clinical scenarios.