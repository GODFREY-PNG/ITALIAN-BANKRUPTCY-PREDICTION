# Create README.md file
cat > README.md << 'EOF'
🏦 Bankruptcy Prediction in Italian Banks
=========================================

📘 Overview
------------
This project focuses on predicting the likelihood of bankruptcy among Italian banks using historical financial data and machine learning.  
The goal is to help financial institutions identify at-risk banks early, minimizing administrative and legal costs through proactive decision-making.

⚙️ Project Workflow
--------------------

### 1️⃣ Data Import & Inspection
- Loaded the dataset from a CSV file.
- Inspected data types, missing values, and inconsistencies.
- Cleaned and preprocessed data using method chaining for efficient transformation.

### 2️⃣ Exploratory Data Analysis (EDA)
- Examined class distribution to detect imbalance.
- Visualized data with boxplots, histograms, and a correlation heatmap.
- Identified relationships between financial indicators and bankruptcy status.

### 3️⃣ Data Preparation
- Split data into training and test sets (80/20).
- Handled class imbalance using oversampling techniques.
- Established a baseline accuracy for model performance comparison.

### 4️⃣ Model Building & Evaluation
- Trained multiple classifiers, with Random Forest as the main model.
- Performed cross-validation and GridSearchCV for hyperparameter tuning.
- Compared models using accuracy, precision, and recall metrics.
- Stored evaluation results in a DataFrame for comparison.

### 5️⃣ Model Interpretation & Impact Analysis
- Analyzed feature importance to identify top predictors of bankruptcy.
- Evaluated outcomes using a confusion matrix and an interactive threshold slider to balance recall and precision.
- Incorporated a cost analysis to simulate real-world financial impacts:
  - False Negatives (FN): Missed bankrupt banks → High administrative costs.
  - False Positives (FP): Wrongly flagged banks → Unnecessary legal costs.

📊 Results
-----------
- The optimized Random Forest model achieved a strong trade-off between recall and precision, ensuring reliable detection of at-risk banks while minimizing false alarms.
- Key predictive features included:
  - ROA (Before Interest & Depreciation After Tax)
  - Liability to Equity Ratio
  - Net Income to Stockholder’s Equity
  - Continuous Interest Rate (After Tax)
  - Persistent EPS (Last Four Seasons)
  - Total Debt / Total Net Worth
- The cost-sensitive evaluation allows banks to balance risk reduction vs. cost efficiency by adjusting the decision threshold.

🧠 Conclusion
--------------
This project demonstrates how machine learning can enhance financial decision-making in the banking sector.  
By combining predictive modeling with cost-based evaluation, financial institutions can better allocate resources, reduce risk exposure, and improve early warning systems for financial distress.

🛠️ Tools & Technologies
-------------------------
Languages: Python  
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn  
Techniques: EDA, Oversampling, Random Forest, Cross-Validation, Grid Search, Confusion Matrix, Feature Importance Analysis, Cost-Sensitive Evaluation
EOF
