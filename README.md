# Nkone_project 1: Advanced EDA & Production-Ready Feature Engineering

## 📌 Project Description
This project implements an enterprise-grade **Input-Process-Output (IPO) technical architecture** to transform raw, noisy cardiovascular health records into a mathematically stable, highly validated dataset ready for machine learning production pipelines. 

Using data derived from the John Smith Heart Disease dataset, this pipeline stabilizes statistical variance, engineers strategic clinical interaction metrics, and programmatically enforces data contracts using strict programmatic schemas.

---

## 🛠️ Data Pipeline Architecture

### 1. Module 1: Input (Outlier Mitigation)
* **Objective:** Neutralize extreme statistical anomalies across continuous variables (`trestbps`, `chol`, `thalach`, `oldpeak`) without removing data rows or introducing sample bias.
* **Methodology:** Applied non-parametric **Interquartile Range (IQR)** thresholds:
  $$Lower Bound = Q1 - 1.5 \times IQR$$
  $$Upper Bound = Q3 + 1.5 \times IQR$$
* **Outcome:** Successfully isolated and handled **57 extreme anomalies**, imputing them with features' global medians to maintain structural data volume at 1,025 observations.

### 2. Module 2: Process (Vectorized Feature Engineering)
To enrich predictive capacity, three high-fidelity, domain-specific features were engineered via vectorized operations:
* **`age_group`**: Maps continuous ages into structural logical tiers (`0`: Young, `1`: Middle-aged, `2`: Senior).
* **`chol_age_ratio`**: Captures age-adjusted metabolic indicator progression.
* **`hr_bps_interaction`**: Computes the spread between peak output (`thalach`) and resting cardiovascular pressure (`trestbps`).

### 3. Module 3: Output (Pandera Schema Validation)
* **Data Contract Validation:** Utilized the **Pandera** framework to strictly enforce structural boundaries, column data types, and logical limits.
* **Artifact Generation:** The verified dataset successfully passed all constraints and exported a pristine file named `heart_disease_cleaned_project1.csv`.

---

## 📂 Project Repository Structure
* `heart.csv` — Raw input dataset containing 1,025 medical rows.
* `Project_1_Notebook.ipynb` — The full Google Colab data science execution script.
* `heart_disease_cleaned_project1.csv` — Final production-ready validated dataset output.

---

## 🚀 How to Run the Environment

### 1. Clone the Project
```bash
git clone [https://github.com/nkonesani-code/Task-1-Nkhensani.git](https://github.com/nkonesani-code/Task-1-Nkhensani.git)
cd Task-1-Nkhensani

