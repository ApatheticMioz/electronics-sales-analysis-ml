# Electronics Sales Analysis & Customer Segmentation for Imtiaz Mall

## Project Overview

This project addresses a business problem for Imtiaz Mall, focusing on analyzing declining sales and customer retention in the electronics section. Using historical customer data (`electronics.json`), this analysis involves comprehensive data preprocessing, Exploratory Data Analysis (EDA), predictive modeling (Linear Regression, Decision Trees), and customer segmentation (K-Means Clustering) to derive actionable insights.

This project was developed as part of the Introduction to Data Science (DS-2001) coursework at FAST NUCES, Islamabad.

## Analysis Pipeline

1.  **Data Acquisition & Preprocessing:**
    * Loaded historical transaction data including customer demographics, purchase history, product details, spending, and dates.
    * Handled missing values using mean imputation for symmetrically distributed numeric columns and mode imputation for skewed numeric columns and categorical data. (Appropriate as missing values were <5% per column).
    * Performed outlier detection using IQR; no significant outliers found.
    * Dropped irrelevant columns (e.g., Customer_ID, Transaction_ID).
    * Encoded categorical variables using One-Hot Encoding.
    * Standardized numerical features using `StandardScaler`.

2.  **Exploratory Data Analysis (EDA):**
    * **Univariate Analysis:** Examined distributions of key variables like Age, Purchase Amount, Purchase Frequency (mostly symmetric).
    * **Bivariate Analysis:** Investigated correlations between variables using heatmaps and scatter plots (found low correlation between Purchase Amount, Brand Affinity, Purchase Frequency, and Age).
    * **Temporal Analysis:** Analyzed trends over time, showing peaks in average spending in October (Fall) and relatively flat purchase frequency throughout the year.

3.  **Predictive Modeling:**
    * **Linear Regression:** Attempted to predict 'Average Spending Per Purchase' using customer demographics and history. The model showed poor performance ($R^2 \approx -0.025$, high MAE/MSE), indicating it wasn't suitable for this specific prediction task with the given data. OLS diagnostics (Residuals vs Fitted, Q-Q plot, Homoscedasticity check, VIF) were performed.
    * **Decision Tree Classifier:** Predicted the binary variable 'Will purchase next month'. Achieved high performance (Accuracy: ~92.7%, Precision: ~96.5%, Recall: ~95.0%, F1: ~95.8%), indicating suitability for this classification task.

4.  **Clustering Analysis:**
    * Applied K-Means clustering to segment customers. The optimal number of clusters (k=4) was determined using the elbow method.
    * Used PCA to reduce dimensionality for visualizing clusters in 2D and 3D.
    * Analyzed cluster characteristics, finding significant differences in Age, Purchase Amount, Average Spending, Days since last purchase, Gender composition, and Brand Affinity across clusters. Found less variation in 'Will Purchase Next Month' likelihood, income levels, and seasonal preferences across clusters.

## Actionable Recommendations (Summary)

Based on the analysis, recommendations were made to Imtiaz Mall, including:
* Targeting customer segments with tailored offers based on spending habits, brand affinity, age, and product preferences.
* Developing gender-specific marketing campaigns.
* Optimizing offers for different purchase frequencies and spending levels.
* Adjusting promotions based on seasonality.
* Focusing on general customer engagement to drive repeat purchases, as purchase intent was similar across clusters.

## Tech Stack

* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Scikit-learn (for `StandardScaler`, `LinearRegression`, `DecisionTreeClassifier`, `KMeans`, `PCA`, metrics), Matplotlib/Seaborn (for visualization), Statsmodels (potentially, for OLS diagnostics).

## Setup

1.  **Clone:** `git clone https://github.com/ApatheticMioz/electronics-sales-analysis-ml.git`
2.  **Install:** `pip install pandas numpy scikit-learn matplotlib seaborn statsmodels` *(Refer to the notebook to see libraries to install)*
3.  **Dataset:** Ensure `electronics.json` is in the directory.

## Usage

Launch and run the notebook file in an environment of your choice. 
