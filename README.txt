🏦 Bankruptcy Prediction in Italian Banks
📘 Project Overview

This project aims to predict the likelihood of bankruptcy among Italian banks using historical financial data and machine learning techniques.
The goal is to help financial institutions minimize administrative and legal costs by accurately identifying at-risk banks early.

⚙️ Steps & Methodology
1️⃣ Data Import & Inspection

Loaded the dataset from a CSV file.

Inspected data types, missing values, and inconsistencies.

Cleaned and preprocessed the dataset using method chaining for efficient data handling.

2️⃣ Exploratory Data Analysis (EDA)

Checked class balance to assess data imbalance.

Created visualizations including boxplots, histograms, and a correlation heatmap to understand relationships between variables.

3️⃣ Data Preparation

Split features and target variables using train-test split (test size = 0.2).

Addressed class imbalance using oversampling techniques.

Computed a baseline accuracy for comparison.

4️⃣ Model Building & Evaluation

Built and evaluated multiple models, including Random Forest as the primary classifier.

Performed cross-validation to compare different classifiers.

Tuned hyperparameters using GridSearchCV, storing results in a DataFrame.

Selected the best-performing model based on accuracy, precision, and recall metrics.

5️⃣ Model Interpretation & Impact Analysis

Plotted top feature importances to identify key predictors of bankruptcy.

Evaluated outcomes with a confusion matrix and an interactive threshold slider to balance recall and precision.

Simulated real-world costs:

False Negatives → Missed bankrupt banks → wasted administrative costs.

False Positives → Wrongly flagged banks → wasted legal costs.

📊 Results

The optimized Random Forest model achieved a strong balance between precision and recall.

The cost-analysis framework helps banks minimize total losses due to misclassification.

🧠 Analysis

The optimized Random Forest model achieved a strong trade-off between recall and precision, ensuring reliable detection of at-risk banks while limiting false alarms.

Feature importance analysis revealed that key predictors of financial distress include:

ROA(B) before interest and depreciation after tax

Liability to Equity

Net Income to Stockholder's Equity

Continuous interest rate (after tax)

Persistent EPS in the Last Four Seasons

Total debt / Total net worth

By adjusting the decision threshold, banks can prioritize risk reduction (recall) or cost efficiency (precision) depending on their strategic goals.

This project demonstrates how machine learning and cost-sensitive evaluation can enhance financial decision-making and improve resource allocation in the banking sector.

🛠️ Tools & Technologies

Languages: Python
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
Techniques: EDA, Oversampling, Random Forest, Cross-Validation, Grid Search, Confusion Matrix Analysis, Hyperparameter Tuning
