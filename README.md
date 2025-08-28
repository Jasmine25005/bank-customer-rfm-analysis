# RFM Analysis for Bank Customer Segmentation

![Python](https://img.shields.io/badge/Python-3.9-blue.svg?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-purple.svg?style=for-the-badge&logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-5.15-green.svg?style=for-the-badge&logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-orange.svg?style=for-the-badge&logo=seaborn)

An in-depth customer segmentation project using the RFM (Recency, Frequency, Monetary) model on a bank transaction dataset. The goal is to identify distinct customer groups to enable targeted and effective marketing strategies.

---

## 📊 Key Visualization: Segment Characteristics

This chart clearly shows the average RFM scores for each customer segment. High-Value customers excel in all three metrics, while Low-Value customers lag significantly, especially in Recency and Frequency.

[_**Important:** Take a screenshot of your final Plotly grouped bar chart and place it here. It's the most powerful summary of your project's findings._]



---

## 🎯 Project Overview

This project performs a comprehensive RFM analysis to segment bank customers into meaningful groups. By analyzing transaction history, we can classify customers into tiers like 'High-Value', 'Mid-Value', and 'Low-Value'. These insights are crucial for businesses to:

* Personalize marketing campaigns.
* Improve customer retention by identifying at-risk customers.
* Optimize resource allocation by focusing on high-value segments.

### **Dataset**

The analysis is based on the **Bank Customer Segmentation** dataset from Kaggle.
* **Source:** [Kaggle Dataset Link](https://www.kaggle.com/datasets/shivamb/bank-customer-segmentation)

---

## ⚙️ Analysis Pipeline

The project follows a structured data science workflow:

1.  **Data Loading & Initial Exploration:** The dataset is loaded, and its basic structure, dimensions, and data types are examined.
2.  **Data Cleaning & Preprocessing:**
    * Standardized the `CustomerID` column (handled mixed types, removed prefixes, and converted to integer).
    * Handled missing values and removed duplicate transactions.
    * Filtered out transactions with zero or negative amounts.
    * Corrected data types, especially for dates.
3.  **Feature Engineering:**
    * Focused the analysis on a specific high-activity region (`MUMBAI`).
    * Created a `TotalAccountBalance` feature for a more holistic monetary view.
4.  **RFM Calculation:**
    * **Recency (R):** Calculated as the number of days since the customer's last transaction.
    * **Frequency (F):** Calculated as the total number of transactions made by each customer.
    * **Monetary (M):** Calculated as the total sum of transaction amounts for each customer.
5.  **RFM Scoring & Segmentation:**
    * Customers were scored on a scale of 1-4 for each RFM metric based on quartiles.
    * A combined `RFM_Score` was created.
    * Customers were segmented into three final tiers: **High-Value**, **Mid-Value**, and **Low-Value**.
6.  **Data Visualization & Insight Generation:**
    * Visualized the distribution of customers across the three value segments.
    * Created a correlation heatmap to understand the relationships between R, F, and M.
    * Developed an interactive bar chart to compare the defining characteristics of each segment.

---

## 💡 Key Findings

* **High-Value Customers:** This group consists of recent, frequent, and high-spending customers. They are the most valuable asset and should be targeted with loyalty programs and exclusive offers.
* **Mid-Value Customers:** This group shows moderate engagement. They represent a significant opportunity and can be nurtured into high-value customers through targeted promotions.
* **Low-Value Customers:** This group is characterized by infrequent and old transactions. They are at risk of churning and require re-engagement campaigns to reactivate their interest.

---

## 🚀 How to Run

To replicate this analysis, follow these steps:

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/Jasmine25005/bank-customer-rfm-analysis.git
    cd rfm-customer-segmentation-python
    ```
2.  **Install dependencies:**
    It's recommended to create a virtual environment first.
    ```sh
    pip install pandas numpy matplotlib seaborn plotly notebook
    ```
3.  **Launch Jupyter Notebook:**
    ```sh
    jupyter notebook
    ```
4.  **Run the notebook:**
    Open the `.ipynb` file and execute the cells.
