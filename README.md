# Hybrid Diabetes Prediction & Clinical Decision Support Pipeline
**A Physician-Facing ML & BI Pipeline bridging Clinical Diagnostics and Predictive AI**

## Clinical Overview & Problem Statement
In clinical practice, early detection of diabetes mellitus (T2DM) is critical to prevent irreversible complications 

**The Solution**
That project designs a **Clinical Decision Support System** pipeline that utilizes a **Random Forest Classifier** trained on **100,000 patients records** to predict diabetic risk.

## Teck Stack & decisions :
**Data Engineering:**Python(`Pandas`,`NumPy`,`Scikit-Learn`)
**BI Visualization:**Power BI Desktop (Interactive Clinical Dashboard)

<img width="1311" height="739" alt="Screenshot 2026-07-16 194551" src="https://github.com/user-attachments/assets/2479ee50-08fb-4543-a429-11f3a7f0d030" />


### 🧹 Clinical Data Cleaning & Mapping:
1. **Smoking History Standardization (Manual Mapping):** 
   In the raw dataset, smoking history contained redundant and overlapping categories (such as 'not current', 'ever', and 'former'). We engineered a clean mapping dictionary to consolidate these clinical categories into 4 standardized statuses: `never`, `current`, `former`, and `No Info` to reduce clinical noise for the machine learning model.

   
  
##  Model Performance & Clinical Error Audit:
Our model achieved **97% overall accuracy** and **94% precision**.

### The Clinical Logic of the Error Audit:
We created a custom `Classification_Status` in Python to isolate and analyze **False Negatives (Type II Errors)** in Power BI, ensuring patients with diabetes aren't missed during screening.

## How to Run Locally
1. Install dependencies: `pip install -r requirements.txt`
2. Run the pipeline: `python src/diabetes_prediction_dataset.ipynb`
