# 📉 Early Bankruptcy Risk Detection for Italian Companies  
### A Cost-Sensitive Machine Learning Approach for Financial Decision-Making

## 1️⃣ Business Problem

Financial institutions face significant costs when corporate bankruptcies are detected too late. These costs include loan defaults, legal proceedings, and administrative overhead. At the same time, overly aggressive risk flagging can lead to unnecessary legal reviews and missed business opportunities.

### Objective
The objective of this project is to support credit risk and financial monitoring teams by predicting the likelihood of bankruptcy among Italian companies, enabling earlier intervention and more cost-effective decision-making.

---
## 2️⃣ Stakeholders & Decisions Supported

### Primary stakeholders
- Credit risk analysts  
- Financial monitoring teams  
- Risk management departments  

### Key decisions supported by the model
- Which companies require enhanced financial monitoring  
- Which firms should be prioritized for early intervention or restructuring  
- How to balance missed bankruptcies versus unnecessary legal actions  

---
## 3️⃣ Data Overview

The dataset contains historical financial ratios and accounting indicators for Italian companies, along with a binary target variable indicating bankruptcy status.

### Key characteristics
- Real-world financial ratios commonly used in credit risk analysis  
- Strong class imbalance, reflecting the rarity of bankruptcy events  
- Presence of correlated and scale-sensitive financial indicators  

--
## 4️⃣ Data Import, Inspection & Cleaning

The data was loaded from a CSV file and systematically inspected to ensure quality and consistency.

### Steps performed
- Verified data types and detected missing or anomalous values  
- Applied preprocessing and cleaning using method chaining for clarity and reproducibility  
- Ensured all features were in a format suitable for downstream modeling  

---
## 5️⃣ Exploratory Data Analysis (EDA)

EDA was conducted with a decision-oriented focus, aiming to uncover early warning signals of financial distress.

### Key questions explored
- Which financial ratios differ most between bankrupt and non-bankrupt firms?  
- Are leverage indicators stronger predictors than profitability metrics?  
- Do bankrupt companies exhibit extreme values or gradual deterioration?  

### Techniques used
- Class distribution analysis to assess imbalance  
- Boxplots and histograms to compare financial indicators  
- Correlation heatmap to identify redundant or highly related features  

---
## 6️⃣ Data Preparation & Baseline Modeling

To ensure robust evaluation, the dataset was split into training and test sets using an 80/20 ratio.

### Preparation steps included
- Addressing class imbalance through oversampling techniques  
- Establishing a baseline model to contextualize performance gains  
- Preserving an untouched test set for final evaluation  

---
## 7️⃣ Modeling Strategy

Multiple classification models were trained and compared, with a focus on balancing predictive performance and practical usability.

### Approach
- Trained several classifiers as benchmarks  
- Selected Random Forest as the primary model due to its strong performance on imbalanced data  
- Applied cross-validation and GridSearchCV for hyperparameter tuning  

### Note on interpretability
Logistic Regression was included as a benchmark due to its transparency, which is often preferred in regulated financial environments.

---
## 8️⃣ Model Evaluation & Metrics

Model performance was evaluated using metrics aligned with real-world risk considerations rather than accuracy alone.

### Metrics emphasized
- Recall (to minimize missed bankruptcies)  
- Precision (to limit unnecessary risk escalation)  
- Confusion matrix analysis to understand error types  

All evaluation results were stored and compared in a structured DataFrame.

--
## 9️⃣ Cost-Sensitive Evaluation & Threshold Optimization

Because different classification errors carry different financial consequences, a cost-based evaluation framework was implemented.

### Assumed cost structure
- **False Negatives (FN):** Missed bankrupt companies → high administrative and legal costs  
- **False Positives (FP):** Incorrectly flagged companies → unnecessary monitoring and legal review costs  

An interactive decision threshold slider was used to:
- Adjust the trade-off between recall and precision  
- Simulate real-world cost implications of different operating points  
- Allow stakeholders to choose thresholds based on risk tolerance and resource availability  

---
## 🔍 Key Predictive Features

Feature importance analysis identified the most influential indicators of bankruptcy risk, including:

- ROA (Before Interest & Depreciation After Tax)  
- Liability to Equity Ratio  
- Net Income to Stockholder’s Equity  
- Continuous Interest Rate (After Tax)  
- Persistent EPS (Last Four Seasons)  
- Total Debt / Total Net Worth  

These features align closely with established financial risk theory, reinforcing model credibility.

---
## 📊 Results & Business Impact

The optimized Random Forest model achieved a strong balance between recall and precision, enabling reliable identification of high-risk companies while keeping false alarms manageable.

### Practical impact
- Risk teams can focus attention on a smaller, higher-risk subset of companies  
- Early detection enables proactive intervention rather than reactive legal action  
- Decision thresholds can be adjusted dynamically to reflect changing economic conditions or institutional risk appetite  

---
## 🧠 Conclusion

This project demonstrates how machine learning can be applied responsibly in financial risk management by combining predictive modeling with cost-sensitive decision analysis.

By framing model outputs around real operational trade-offs, the approach moves beyond pure prediction and supports actionable, data-driven decision-making in the banking and financial services sector.

---
## 🚀 Next Steps & Extensions

Potential improvements include:
- Incorporating macroeconomic indicators to capture systemic risk  
- Monitoring model performance and data drift over time  
- Deploying the model via an API or dashboard for analyst use  
- Integrating predictions into credit approval or monitoring workflows  

---
## 🛠️ Tools & Technologies

**Language:** Python  

**Libraries:**  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  

**Techniques:**  
EDA, Oversampling, Random Forest, Cross-Validation, Grid Search,  
Confusion Matrix Analysis, Feature Importance, Cost-Sensitive Evaluation
