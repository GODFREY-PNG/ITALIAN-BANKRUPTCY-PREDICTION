🏦 Bankruptcy Prediction in Italian Banks
Project Overview
This project aims to predict the likelihood of bankruptcy among Italian banks using historical financial data and machine learning techniques. The goal is to help financial institutions minimize administrative and legal costs by accurately identifying at-risk banks early.
Steps & Methodology
Data Import & Inspection
Loaded the dataset from a CSV file.


Inspected data types, missing values, and inconsistencies.


Cleaned and preprocessed the dataset using method chaining for efficient data handling.


Exploratory Data Analysis (EDA)


Checked class balance to assess data imbalance.


Created visualizations including boxplots, histograms, and a correlation heatmap to understand relationships between variables.


Data Preparation


Split features and target variables using train-test split (test size = 0.2).


Addressed class imbalance using oversampling techniques.


Computed a baseline accuracy for comparison.


Model Building & Evaluation


Built and evaluated multiple models, including Random Forest as the primary classifier.


Performed cross-validation to compare different classifiers.


Tuned hyperparameters using GridSearchCV, storing results in a DataFrame.


Selected the best-performing model based on accuracy, precision, and recall metrics.


Model Interpretation & Impact Analysis


Plotted top feature importances to identify key predictors of bankruptcy.


Evaluated model outcomes with a confusion matrix and an interactive threshold slider to find the “sweet spot” between recall and precision.


Simulated real-world costs:


False Negatives → Wasted administrative costs (banks not flagged but go bankrupt).


False Positives → Wasted legal costs (banks wrongly flagged as bankrupt).
6. Results
Optimized Random Forest model achieved a strong balance between precision and recall.


Cost-analysis framework helps banks minimize total losses due to misclassification.
7.Analysis
The optimized Random Forest model achieved a strong trade-off between recall and precision, ensuring reliable detection of at-risk banks while limiting false alarms.
Feature importance analysis revealed that; ROA(B) before interest and depreciation after tax,Liability to Equity,Net Income to Stockholder's Equity,Continuous interest rate (after tax),Persistent EPS in the Last Four Seasons,Total debt/Total net worth were key predictors of financial distress.
By adjusting the decision threshold, banks can prioritize risk reduction (recall) or cost efficiency (precision) depending on their strategic goals.
This project demonstrates how machine learning and cost-sensitive evaluation can enhance financial decision-making and improve resource allocation in the banking sector.





 Tools & Technologies
Languages: Python


Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn


Techniques: EDA, Oversampling, Random Forest, Cross-Validation, Grid Search, Confusion Matrix Analysis,hyperparameters tuning





