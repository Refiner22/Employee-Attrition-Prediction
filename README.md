# Employee-Attrition-Prediction
## Situation
Employee attrition, or staff turnover, refers to employees leaving an organization voluntarily or involuntarily. High attrition rates can increase costs related to recruitment, onboarding, and training, while also reducing overall productivity and employee morale.

Organizations need to not only understand who is leaving but also why they are leaving. HR analytics can play a critical role by leveraging data-driven insights to identify risk factors and predict attrition in advance.

### This project was initiated to:

Explore employee data to identify patterns related to attrition.

Use machine learning models to build a predictive system for attrition.

Provide actionable recommendations to HR departments for employee retention.

## Task

### The main objectives of this project were:

Data Exploration & Understanding

Identify the composition of the workforce, attrition rates, and key demographics.

Detect trends, such as attrition by department, job role, salary level, or work-life balance.

Data Preprocessing

Handle missing values, imbalances, and outliers.

Prepare categorical and numerical features for modeling.

Model Development

Build machine learning models to predict whether an employee is at risk of leaving.

Optimize model parameters to ensure the best balance between recall (catching true attrition cases) and precision (avoiding false positives).

Evaluation & Insights

Compare model performance using multiple evaluation metrics.

Provide business-oriented interpretations of the results (not just technical accuracy).

## Action

To address the above tasks, the following actions were performed:

1. Data Understanding & EDA

Imported HR dataset (IBM Employee Attrition dataset).

Checked data types, missing values, and overall dataset shape.

Visualized attrition distribution across key features:

Job Role (e.g., sales reps showed higher attrition).

Work-Life Balance (poor balance correlated with leaving).

Overtime (employees with frequent overtime had higher attrition).

Salary Levels (low-income employees had higher turnover).

2. Data Preprocessing

Cleaning: Removed irrelevant or duplicate records.

Encoding: Converted categorical variables (e.g., Gender, JobRole) into numeric values using one-hot encoding and label encoding.

Scaling: Standardized continuous variables like MonthlyIncome and YearsAtCompany.

Class Imbalance Handling: Since attrition cases were fewer than non-attrition, applied SMOTE (Synthetic Minority Oversampling Technique) to balance classes.

3. Feature Engineering

Derived new features such as:

Tenure groups (short, medium, long stayers).

Age buckets (early career, mid-career, late career).

Selected key features based on correlation and feature importance analysis.

4. Modeling

Implemented and compared multiple models:

Logistic Regression – baseline model for interpretability.

Decision Tree – for rule-based analysis.

Random Forest – robust ensemble method.

XGBoost – advanced boosting algorithm with higher predictive power.

Used GridSearchCV and RandomizedSearchCV for hyperparameter tuning.

Trained models on 70% of the dataset and validated on the remaining 30%.

5. Evaluation

Metrics considered: Accuracy, Precision, Recall, F1-score, and ROC-AUC.

Generated confusion matrices to examine false positives and false negatives.

Plotted ROC curves to compare model performance.

Random Forest and XGBoost outperformed other models with higher recall and balanced accuracy.

## Result

The project delivered both technical outcomes and business insights:

Technical Outcomes

Random Forest achieved strong performance with ~87% accuracy and a high ROC-AUC score.

XGBoost showed slightly better generalization with improved recall on attrition cases.

Identified top predictive features influencing attrition:

Overtime

Job Satisfaction

Monthly Income

Years at Company

Work-Life Balance

Business Insights

Employees with frequent overtime and low job satisfaction are more likely to leave.

Mid-level employees (3–6 years of tenure) showed higher attrition risk compared to very new hires or long-tenured staff.

Salary and career progression opportunities strongly affect retention.

HR teams should focus on work-life balance initiatives, fair compensation, and career development programs to reduce turnover.

## Impact

Provides a data-driven decision support tool for HR managers.

Helps organizations anticipate attrition trends and implement preventive measures.

Potential integration into HR dashboards for real-time attrition risk prediction.
