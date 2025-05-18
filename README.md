

## 📘 Customer Lifetime Value (LTV) Prediction

This project predicts **Customer Lifetime Value (LTV)** using machine learning techniques based on historical transaction data from an e-commerce business. The goal is to segment customers by value and help businesses optimize marketing efforts and improve profitability.

---

### 📁 Dataset Used

* **Name:** `online-retail.csv`
* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail)
* **Description:** Contains retail transaction data from a UK-based online retailer from 2010 to 2011.

---

### 🧠 Problem Statement

Businesses need to understand which customers are most valuable in order to allocate marketing budgets efficiently. This project estimates the future monetary value each customer will contribute using **RFM (Recency, Frequency, Monetary)** metrics and **AOV (Average Order Value)**, then applies a regression model to predict LTV.

---

### 🛠 Tools & Technologies

* **Python** – Data analysis and modeling

  * Pandas, NumPy, Matplotlib, Seaborn
  * XGBoost (XGBRegressor)
  * Scikit-learn
* **Power BI** – Dashboard for customer segmentation and insights
* **Jupyter Notebook** – Code and experimentation
* **Microsoft Word** – Final project report

---

### 🔄 Workflow

1. **Data Cleaning**:

   * Removed missing CustomerIDs, negative quantities or prices.
   * Created `TotalAmount = Quantity × UnitPrice`.

2. **Feature Engineering**:

   * Calculated RFM features per customer.
   * Derived AOV = Monetary / Frequency.

3. **Modeling**:

   * Split data into training and test sets.
   * Trained XGBoost regression model to predict `Monetary` as LTV proxy.

4. **Evaluation**:

   * Metrics: MAE, RMSE
   * Predicted values exported to `predicted_ltv.csv`.

5. **Dashboard**:

   * Visualized in Power BI with:

     * Bar chart by LTV segment
     * Histogram of LTV distribution
     * KPI cards (Avg Recency, Frequency, AOV)
     * Slicers for dynamic filtering

---

### 📊 Output

* `models/ltv_model.pkl` – Trained model
* `output/predicted_ltv.csv` – Predictions with LTV values
* `Customer_LTV_Dashboard.pbix` – Interactive Power BI report
* `LTV_Prediction_5_Page_Report.pdf` – Final report for submission

---

### 📌 Key Insights

* High-value customers buy more frequently and recently.
* Segmenting customers enables better targeting and ROI.
* Predictive modeling helps prioritize retention efforts.

---

### 🚀 Future Enhancements

* Add behavioral features or product-level analysis
* Use LSTM for time-based predictions
* Integrate real-time data and dashboard refresh

