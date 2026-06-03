# Project Title: Predicting House Prices with Linear Regression

## 📌 Project Overview
This project was developed as a part of my **Data Analytics Internship** at **Oasis Infobyte**. The main objective is to build a predictive machine learning model using **Multiple Linear Regression** to estimate house prices in the Delhi region based on various physical and structural features. 

The model helps identify which key factors (such as area, number of bedrooms, bathrooms, air conditioning, and location status) significantly impact property valuation, allowing real estate firms or buyers to quantitatively relate and accurately optimize property prices.

---

## 📊 Dataset Description
The dataset used is `Housing.csv`, which contains **545 entries** and **13 data columns**. The features include:
* **Target Variable:** 
  * `price`: The sale price of the house.
* **Numerical Features:** 
  * `area`, `bedrooms`, `bathrooms`, `stories`, `parking`.
* **Categorical Features:** 
  * `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`, `furnishingstatus`.

---

## 🛠️ Tools & Technologies Used
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:**
  * **Data Manipulation:** `pandas`, `numpy`
  * **Data Visualization:** `matplotlib`, `seaborn`
  * **Statistical & ML Modeling:** `statsmodels`, `scikit-learn`

---

## 🚀 Steps Performed

### 1. Data Loading & Inspection
* Imported the dataset using Pandas dataframe tracking.
* Evaluated data dimensions (`shape`) and structural integrity (`info()`), confirming that the dataset contains **zero missing/null values**.
* Handled statistical descriptions with `.describe()` to observe standard spread, minimums, and maximum values.

### 2. Exploratory Data Analysis (EDA)
* Built a comprehensive `pairplot` to visually correlate all continuous variables with property prices.
* Leveraged categorical `boxplots` to verify variance in prices against binary qualitative variables (e.g., assessing price margins for houses with vs. without air conditioning or main road access).

### 3. Data Preparation & Feature Engineering
* **Binary Mapping:** Converted text fields containing `"yes"` or `"no"` (such as `mainroad`, `guestroom`, `basement`, `airconditioning`, etc.) into numerical elements (`1` and `0`).
* **Dummy Variables (One-Hot Encoding):** Split the categorical multi-level variable `furnishingstatus` into individual features (`semi-furnished`, `unfurnished`), safely dropping the first level to avoid the multi-collinearity trap.

### 4. Data Splitting & Feature Scaling
* Separated the data into training and test datasets.
* Applied scaling mechanisms using `MinMaxScaler` on numeric elements to prevent layout imbalances where features with larger scales skew model coefficients.

### 5. Model Training & Diagnostics
* Established a Multiple Linear Regression line using `statsmodels` / `sklearn`.
* Monitored feature significance metrics (such as p-values and VIF scores) to eliminate redundant variables and fine-tune structural efficiency.

### 6. Model Evaluation
* Transformed and projected predictions onto the unseen testing subset (`X_test`).
* Validated results using actual vs. predicted values through scatter plots (`y_test vs y_pred`), proving an accurate and strongly linear correlation trend.

---

## 📈 Key Outcomes & Visuals
* The project successfully proves a positive regression slope, demonstrating that an increase in square-foot area, bathroom counts, and premium additions like air conditioning directly act as primary catalysts for high property valuation.
* The final scatter plot showcases balanced residual bounds, confirming the model fulfills standard linear homoscedasticity assumptions.

---

## 🧑‍💻 How to Run This Project
1. Clone this repository:
```bash
   git clone [https://github.com/YOUR_GITHUB_USERNAME/OIBSIP_DataAnalytics_05.git](https://github.com/YOUR_GITHUB_USERNAME/OIBSIP_DataAnalytics_05.git)
