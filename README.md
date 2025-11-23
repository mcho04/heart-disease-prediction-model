📘 README – Heart Disease Prediction (KNN Model)

🩺 Project Overview  
This project applies a K-Nearest Neighbors (KNN) machine learning model to predict Coronary Artery Disease (CAD) using key clinical indicators. The analysis is based on a medically validated dataset and aims to support early detection of heart disease through data-driven methods.

📊 Dataset & Preprocessing  
- Measurements include age, sex, cholesterol, ST depression, exercise-induced angina, fluoroscopy results, and more.  
- Steps: convert character variables (e.g., `ca`, `thal`) to numeric; create a binary `diagnosis` column (1 = disease present, 0 = none); remove missing rows with `na.omit()`.

🧭 Selected Predictors  
- Age, sex, exercise-induced angina (`exang`), ST depression (`oldpeak`), number of major vessels with calcium (`ca`).  
- These are clinically validated indicators of CAD.

🧮 Modeling Approach  
- Trained a KNN classifier to separate healthy vs. diseased patients.  
- Tuned K for best performance and evaluated with accuracy and a confusion matrix.

✅ Results  
- High overall accuracy.  
- 90.1% accuracy when predicting no disease.  
- 76.9% accuracy when predicting presence of disease (36 of 109 illness cases misclassified).

🔍 Interpretation  
- Strong at flagging patients without CAD.  
- Lower sensitivity for true disease cases; more predictors or advanced models could improve recall.

🚀 Future Directions  
- Improve sensitivity for severe CAD cases.  
- Compare KNN with more advanced ML algorithms.  
- Conduct real-world clinical validation.  
- Evaluate cost-effectiveness in healthcare settings.

📌 Conclusion  
The KNN approach is effective for general CAD prediction and shows promise as a decision-support tool, but further refinement is needed before applying it to high-risk scenarios.
