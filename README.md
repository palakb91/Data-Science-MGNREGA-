# Data-Science-MGNREGA-
# 📘 MGNREGA Employment Generated Analysis (India Data Portal)

This project analyzes the **employment generated under the Mahatma Gandhi National Rural Employment Guarantee Act (MGNREGA)** using open government data from the **India Data Portal**.  
It applies various **Machine Learning algorithms** to uncover insights, predict trends, and identify factors influencing rural employment generation across India.

---

## 🌐 Dataset Information

- **Dataset Name:** Employment Generated (Gram Panchayat Level, Year-wise)  
- **Source:** [India Data Portal - MGNREGA Employment Generated Dataset](https://indiadataportal.com/p/mgnrega-mahatma-gandhi-national-rural-employment-guarantee-act/r/mord-mgnrega_employment_generated-gp-yr-aaa)  
- **Organization:** Ministry of Rural Development (MoRD), Government of India  
- **Description:**  
  Contains yearly employment data across Gram Panchayats, including:
  - Total job cards issued  
  - Employment offered per household  
  - Employment generated per person  
  - Work demand and availability metrics  
  - Number of beneficiaries (including disabled individuals)

---

## 🎯 Objective

To analyze, model, and visualize rural employment trends in India using the MGNREGA dataset — and identify the key factors that drive employment generation at the local level.

---

## 🧠 Models and Methods Applied

### 1️⃣ Simple Linear Regression
- **Goal:** Understand the relationship between *registered households (reg_hh)* and *employment persondays generated (emp_avail_tot_persondays)*.  
- **Result:** Positive correlation — as registered households increase, employment generation also rises.  
- **Insight:** A clear upward trend validates that higher participation leads to greater employment opportunities.

---

### 2️⃣ Multiple Linear Regression
- **Goal:** Predict total employment generated using multiple features like `emp_avail_hh`, `emp_offer_hh`, and `emp_demand_hh`.  
- **R² Score:** ~0.85  
- **RMSE:** Low error margin, strong prediction accuracy.  
- **Insight:** Employment per household and employment offered are the most influential factors.

---

### 3️⃣ K-Means Clustering (with Elbow Method)
- **Goal:** Identify patterns and group similar regions based on employment statistics.  
- **Optimal K:** 3 clusters.  
- **Insight:**  
  - **Cluster 2:** High-performing regions with strong employment indicators.  
  - **Cluster 1:** Medium-performing areas.  
  - **Cluster 0:** Low-performing or underdeveloped regions.  
- **Use Case:** Helps policymakers focus on low-performing districts.

---

### 4️⃣ Decision Tree Classification
- **Goal:** Classify areas based on *disabled beneficiaries* using employment-related factors.  
- **Accuracy:** ~80%  
- **Key Factors:** `emp_avail_pers`, `emp_avail_hh`  
- **Insight:** High employment availability increases the count of disabled beneficiaries.  
- **Visualization:** Decision tree diagram showing top-level decision paths.

---

### 5️⃣ Random Forest Classification
- **Goal:** Improve prediction robustness and interpret key employment features.  
- **Accuracy:** ~83–85%  
- **Top Features:** `emp_offer_hh`, `emp_avail_hh`, `reg_hh`  
- **Insight:** Confirms employment availability and offers are consistent predictors across models.

---

### 6️⃣ Logistic Regression
- **Goal:** Categorize regions into *Low, Medium, and High* disabled beneficiary classes.  
- **Accuracy:** ~73%  
- **Findings:**  
  - Medium & High classes predicted more accurately.  
  - Employment features strongly influence classification.  
- **Insight:** Areas with higher work availability and job cards show higher beneficiary engagement.

---

### 7️⃣ DBSCAN Clustering
- **Goal:** Discover natural groupings and detect outlier regions.  
- **Result:** Detected multiple clusters and isolated outliers (unusual employment patterns).  
- **Insight:**  
  - Outliers represent regions with either extremely high or very low employment generation.  
  - DBSCAN effectively highlights irregular data points for further investigation.

---

## 📈 Technologies & Libraries Used

| Category | Tools / Libraries |
|-----------|------------------|
| **Language** | Python 3 |
| **Data Handling** | pandas, numpy |
| **Visualization** | matplotlib, seaborn |
| **Modeling** | scikit-learn, xgboost |
| **Preprocessing** | StandardScaler, LabelEncoder |
| **Dimensionality Reduction** | PCA |
| **Environment** | Google Colab / Jupyter Notebook |

---

## 📊 Key Insights

✅ Employment availability per household (`emp_avail_hh`) and per person (`emp_avail_pers`) are the strongest indicators of job generation success.  
✅ Districts with higher `emp_offer_hh` values achieve better employment rates and more beneficiary inclusion.  
✅ Clustering separates regions into *high*, *medium*, and *low* employment categories.  
✅ Classification models consistently identify employment features as primary predictors of program performance.  
✅ Outlier analysis (DBSCAN) helps pinpoint regions requiring policy attention.

---

## 📚 Conclusion

The project successfully demonstrates how **Machine Learning can analyze public employment data** to reveal meaningful socioeconomic insights.  
Findings show that **employment offer and availability directly influence rural job generation and beneficiary inclusion** under MGNREGA.  
These models can help policymakers identify underperforming regions and allocate resources more effectively to enhance employment impact across India.

---

## 📂 Project Structure

