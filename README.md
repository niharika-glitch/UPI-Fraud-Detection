# UPI-Fraud-Detection


## Project Overview
This project focuses on identifying fraudulent online transactions within a simulated UPI environment. Leveraging a large-scale dataset of over 6.3 million transactions, the project implements a robust machine learning pipeline—from advanced feature engineering to ensemble modeling to distinguish between legitimate and fraudulent activities.

The primary challenge addressed is the extreme class imbalance (fraudulent transactions make up <0.2% of the data), which is handled using specific algorithmic weighting and performance-focused metrics.

## Key Features & Methodology
- **Data Preprocessing**: Focused analysis on high-risk transaction types to reduce noise.
- Advanced Feature Engineering:
    - Temporal Analysis: Extracted transaction hours and created an is_night flag to capture high risk windows.
    - Balance Dynamics: Derived amount_ratio and balance change features to identify account emptying patterns.
    - Zero-Balance Tracking: Flags for newly created or suspicious accounts with no initial balance.
- **Machine Learning Models**:
    - XGBoost Classifier: Utilized for its speed and performance on structured data.
    - Decision Trees: Used for baseline modeling and rule visualization.
    - Random Forest: Achieved the highest performance by mitigating overfitting and handling non-linear relationships.
- Handling Imbalance: Implemented class_weight adjustments to prioritize the detection of rare fraud cases.

## Technical Stack
- Language: Python
- Libraries: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
- Environment:  Jupyter Notebook

## Results
The Random Forest model emerged as the superior classifier, achieving:
- **Accuracy**: 99.99%
- **Recall**: ~1.00 (Critical for fraud detection to ensure no fraud goes undetected)
- **F1-Score**: 1.00
