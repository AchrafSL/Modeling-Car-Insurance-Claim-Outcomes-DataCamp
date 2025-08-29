# Modeling Car Insurance Claim Outcomes

This project builds a predictive model for On the Road car insurance to identify which customers are likely to make a claim during their policy period. Given the company's limited machine learning infrastructure, the goal is to find the **single most predictive feature** that delivers the highest model accuracy. The analysis uses logistic regression on a cleaned customer dataset to determine the optimal simple model for potential deployment.

This project was completed using DataCamp’s Datalab environment.

---

## 🎯 Project Objectives

- Load and explore customer data related to car insurance claims
- Handle missing values in key variables
- Train individual logistic regression models using **each feature separately**
- Evaluate model performance by **accuracy**, calculated using a **confusion matrix**
- Identify the **single best-performing feature** for predicting insurance claims

---

## 🗃️ Dataset Overview

The data comes from a single CSV file:

| File                                | Description                                   |
|-------------------------------------|-----------------------------------------------|
| [`car_insurance.csv`](./data/car_insurance.csv) | Customer profiles and claim history |

### Final Dataset Columns

| Column                 | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `id`                   | Unique client identifier                                                    |
| `age`                  | Client's age group: 0 (16–25), 1 (26–39), 2 (40–64), 3 (65+)                |
| `gender`               | Client's gender: 0 (Female), 1 (Male)                                       |
| `driving_experience`   | Years with a license: 0 (0–9), 1 (10–19), 2 (20–29), 3 (30+)                |
| `education`            | Level of education: 0 (No education), 1 (High school), 2 (University)       |
| `income`               | Income level: 0 (Poverty), 1 (Working class), 2 (Middle class), 3 (Upper class) |
| `credit_score`         | Credit score (continuous, 0 to 1)                                           |
| `vehicle_ownership`    | Ownership status: 0 (Financing), 1 (Owns vehicle)                           |
| `vehicle_year`         | Vehicle registration year: 0 (Before 2015), 1 (2015 or later)               |
| `married`              | Marital status: 0 (Not married), 1 (Married)                                |
| `children`             | Number of children                                                          |
| `postal_code`          | Client's postal code                                                        |
| `annual_mileage`       | Annual miles driven (numeric)                                               |
| `vehicle_type`         | Type of car: 0 (Sedan), 1 (Sports car)                                      |
| `speeding_violations`  | Number of speeding tickets                                                  |
| `duis`                 | Number of DUI offenses                                                      |
| `past_accidents`       | Number of previous accidents                                                |
| `outcome`              | Target variable: 0 (No claim), 1 (Made claim)                               |

---

## 🔍 Key Findings

- ✅ **Best predictive feature**: `driving_experience`  
- 📊 **Highest model accuracy**: **77.71%**  
- 🧠 Among all individual features, **driving experience** was the strongest predictor of whether a customer would make a claim
- 🛠️ Missing values in `credit_score` (9.82%) and `annual_mileage` (9.57%) were imputed using the **median** value

---

## 🛠️ Tools Used

- **Python**
- **pandas** for data loading and preprocessing
- **statsmodels** (`logit`) for logistic regression modeling
- **NumPy** for numerical operations
- **Jupyter Notebook / DataLab** for analysis and visualization

---

## 📌 How to Use

1. Clone or download this repository
2. Place the `car_insurance.csv` file in the `/data` folder
3. Open the notebook [`Modeling_Car_Insurance_Claim_Outcomes.ipynb`](./Modeling_Car_Insurance_Claim_Outcomes.ipynb) in Jupyter or any compatible environment
4. Run the cells to reproduce the analysis
5. Modify the modeling approach to test combinations of features or alternative algorithms (e.g., decision trees)

---

## ✍️ Author

Project by **Achraf Salimi** — part of an ongoing journey to build and showcase data science skills for real-world business impact.