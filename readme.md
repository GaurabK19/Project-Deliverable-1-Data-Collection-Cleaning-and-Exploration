# Advanced Data Mining Project – Deliverable 1

**Student Name:** Gaurab Karki  
**Course:** 2025 Fall - Advanced Big Data and Data Mining (MSCS-634-B01)
**Dataset:** Healthcare Dataset (Kaggle - Prasad22)  
**Source:** [https://www.kaggle.com/datasets/prasad22/healthcare-dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)

---

## Project Overview

This project focuses on applying advanced data mining techniques to a real-world healthcare dataset. The objective is to prepare, clean, explore, and analyze the data to extract meaningful insights, which will guide future modeling tasks such as regression, classification, clustering, and association rule mining.

Deliverable 1 involves **data collection, cleaning, and exploratory analysis** to ensure the dataset is ready for predictive modeling.

---

## Dataset Summary

The Healthcare Dataset contains patient-level records from hospitals, including demographic, clinical, and billing information. Key features include:

- `Name`  
- `Age`  
- `Gender`  
- `Blood Type`  
- `Medical Condition`  
- `Date of Admission`  
- `Doctor`  
- `Hospital`  
- `Insurance Provider`  
- `Billing Amount`  
- `Room Number`  
- `Admission Type`  
- `Discharge Date`  
- `Medication`  
- `Test Results`

The dataset has over **10,000 records** and **12+ attributes**, providing a rich mix of numerical, categorical, and temporal data suitable for multiple data mining tasks.

---

## Data Cleaning Steps

1. **Handling Missing Values**
   - Numeric columns (`Age`, `Billing Amount`) were imputed using the **median**.  
   - Categorical columns (`Gender`, `Hospital`, `Medical Condition`, etc.) were imputed using the **mode**.  
   - Rows with missing critical dates (`Date of Admission` or `Discharge Date`) were removed.

2. **Removing Duplicates**
   - Duplicate records were detected and removed to maintain data integrity.

3. **Addressing Noisy Data**
   - Standardized categorical text (capitalization, spacing).  
   - Removed unrealistic numeric values (`Age < 0 or > 120`, `Billing Amount <= 0`).  
   - Outliers were identified and capped using winsorization to prevent skewing analyses.

---

## Exploratory Data Analysis (EDA) Insights

1. **Age and Billing Relationship**
   - Older patients tend to have higher billing amounts; Age is a strong predictor for regression.

2. **Hospital and Medical Condition Patterns**
   - Certain hospitals have higher patient volumes; common medical conditions can be used in classification or clustering.

3. **Billing Variability**
   - High variation and extreme billing values were capped for stability in modeling.

4. **Gender Differences**
   - Small differences in billing exist across genders, which may inform categorical features in models.

5. **Categorical Feature Imbalances**
   - Imbalances in `Medical Condition`, `Hospital`, and `Insurance Provider` suggest potential stratification or weighting in modeling.

6. **Potential Clusters**
   - Patients could be grouped by Age, Billing Amount, and Medical Condition for segmentation analysis.

---

## Future Modeling Guidance

| Insight | Modeling Implication |
|---------|-------------------|
| Age vs Billing correlation | Use Age as predictor in regression tasks |
| Frequent medical conditions | Encode categorical features for classification/clustering |
| High billing variability | Handle outliers to stabilize regression models |
| Gender differences | Include Gender as categorical predictor |
| Imbalanced categorical features | Consider stratified sampling or weighting |
| Potential clusters | Apply clustering for patient segmentation |

---

## Challenges and Decisions

- Missing data required careful imputation to maintain dataset integrity.  
- Outliers and unrealistic values in numeric columns were addressed to avoid biasing models.  
- Standardizing categorical text ensured consistency for downstream encoding and analysis.  
- Balancing interpretability and completeness was important during data cleaning and preprocessing.

---

## Conclusion

The Healthcare Dataset has been cleaned, processed, and explored to extract key insights. The dataset is now ready for feature engineering and modeling tasks, including regression, classification, clustering, and association rule mining in subsequent deliverables.