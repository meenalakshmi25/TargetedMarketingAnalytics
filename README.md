# **Customer Segmentation for Targeted Marketing within the Banking Sector**  

This repository contains the full implementation of an MSc Business Analytics dissertation focused on customer segmentation using machine learning techniques. The project aims to identify distinct customer groups within the banking sector to enable more effective and personalized marketing strategies.

---

### **Project Overview**

- **University**: University of Greenwich  
- **Course**: MSc Business Analytics  
- **Topic**: Customer Segmentation for Targeted Marketing  
- **Dataset**: UCI Bank Marketing Dataset  
- **Tools Used**: Python, Jupyter Notebook, Scikit-learn, Matplotlib, Seaborn  

---

## Analysis Steps:

1.  **Data Loading and Basic Insights**: The dataset was loaded and basic information such as shape, columns, and initial rows were inspected.
2.  **Data Processing**: Categorical features were encoded and a numerical representation for the 'month' was created.
3.  **Exploratory Data Analysis (EDA)**: Visualizations were generated to understand the distribution of various features and their relationship with the target variable ('y').
4.  **Dataset Preprocessing & Feature Engineering**:
    *   Data was scaled using `StandardScaler`.
    *   Principal Component Analysis (PCA) was applied for dimensionality reduction and visualization.
    *   K-Means clustering was performed to segment customers, and the silhouette score was calculated to evaluate the clustering. The average profile of each cluster was also analyzed.
5.  **Classification Modeling**:
    *   The data was split into training and testing sets.
    *   Two classification models, Random Forest and XGBoost, were trained and evaluated using various metrics such as Accuracy, Precision, Recall, F1 Score, and ROC-AUC.
    *   Feature importances were visualized for both models.
6.  **Model Comparison**: The performance metrics of the Random Forest and XGBoost models were compared.

---

## Key Findings:

*   The dataset contains customer information with a target variable 'y' indicating subscription status.
*   EDA revealed insights into the distribution of features like age, balance, job categories, and how factors like marital status and previous outcome relate to subscription rates.
*   PCA showed some separation based on the target variable, but the explained variance was relatively low with just two components.
*   K-Means clustering with 4 clusters resulted in a silhouette score of approximately 0.10, suggesting that the clusters are not well-separated.
*   Both Random Forest and XGBoost models achieved high accuracy (around 90%), but precision and recall for the positive class (subscribed) were lower, indicating a challenge in correctly identifying all subscribed customers due to the class imbalance observed in the target distribution.
*   XGBoost showed slightly better performance across most metrics compared to Random Forest.
*   Feature importance analysis identified the most influential features for predicting subscription.

---

This analysis provides a starting point for understanding customer behavior and building predictive models. Further work could involve exploring different clustering algorithms, optimizing model hyperparameters, or addressing the class imbalance.
