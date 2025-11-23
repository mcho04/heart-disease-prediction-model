:heartpulse: Heart Disease Prediction (KNN)
 Predictive modeling workflow for Coronary Artery Disease (CAD) using a K-Nearest Neighbors classifier, summarized from `heart_disease_prediction.html`.

Project scope :spiral_notepad:
- Goal: predict CAD presence from routine clinical indicators and assess if a simple KNN model can support early diagnosis.
- Data: 14-column dataset (`data/heart_disease.xlsx`) compiled from Cleveland Clinic, Hungarian Institute of Cardiology, University Hospital in Zurich, and VA Long Beach studies.
- Report files: `heart_disease_prediction.ipynb` (analysis notebook in R) and the rendered `heart_disease_prediction.html` (full narrative, charts, and tables).

Methodology highlights :wrench:
- Cleaning: cast `ca` and `thal` to numeric; add `diagnosis` (1 = disease present, 0 = none); drop missing rows.
- Feature selection: removed low-signal columns such as `trestbps`, `chol`, and `fbs`; modeled with clinically meaningful predictors including age, sex, chest pain type (`cp`), exercise-induced angina (`exang`), ST depression (`oldpeak`), slope, major vessels with calcium (`ca`), thalassemia (`thal`), resting ECG (`restecg`), and max heart rate (`thalach`).
- Split and resampling: 80/20 stratified train/test split; 5-fold cross-validation on the training set to tune K.
- Model tuning: grid search over candidate neighbors; best-performing K = 25.

Results (from the HTML report) :bar_chart:
- Overall accuracy: ~86%.
- When the model predicts heart disease, precision is ~90.1%.
- Recall for true disease cases: ~76.9% (36 of 109 positives missed), indicating room to improve sensitivity.
- Confusion matrix and K-vs-accuracy plots are included in `heart_disease_prediction.html`.

Interpreting performance :mag:
- Strength: reliably flags patients without CAD, reducing unnecessary follow-up.
- Limitation: under-detects some positive cases, so it should complement (not replace) richer diagnostic workflows or additional features.

How to reproduce :computer:
- Open `heart_disease_prediction.ipynb` in Jupyter and run all cells (R kernel). Required R packages: `tidyverse`, `tidymodels`, `readxl`, `tidyclust`, `repr`, `GGally`.
- Or review the rendered findings directly in `heart_disease_prediction.html`.

Future work (from the report) :bulb:
- Improve sensitivity for severe CAD cases by expanding predictors or testing alternative algorithms/ensembles.
- Benchmark KNN against other models and validate on real clinical cohorts.
- Analyze cost-effectiveness of deploying the model alongside standard diagnostics.
