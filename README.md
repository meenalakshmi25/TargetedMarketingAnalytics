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
    *   Agglomerative Clustering:
Agglomerative Clustering was applied as an alternative clustering technique. This hierarchical method does not require the number of clusters to be specified upfront.
The dendrogram was plotted to visualize the hierarchical structure of clusters, and an appropriate cut-off was chosen to form clusters.
Similar to K-Means, the silhouette score was calculated for Agglomerative Clustering to assess the separation and compactness of the clusters.
The average profile of each cluster was analyzed to compare the segments formed by Agglomerative Clustering with those obtained from K-Means, providing deeper insights into customer behavior.
5.  **Classification Modeling**:
    *   The data was split into training and testing sets.
    *   Two classification models, Random Forest and XGBoost, were trained and evaluated using various metrics such as Accuracy, Precision, Recall, F1 Score, and ROC-AUC.
    *   Feature importances were visualized for both models.
6.  **Model Comparison**: The performance metrics of the Random Forest and XGBoost models were compared.

---

## Key Findings:

Key Findings

Dataset Overview:

The dataset contains various customer features, with a target variable 'y' indicating subscription status to a term deposit (subscribed = 1, not subscribed = 0).

Key features include demographic information (e.g., age, job, marital status), financial information (balance, housing loan, credit default), and engagement data (e.g., contact, previous outcome, duration of contact).

Exploratory Data Analysis (EDA):

Initial EDA provided valuable insights into the distribution of features such as age, balance, and job categories.

Marital status and previous outcome were found to have significant relationships with the likelihood of subscribing to the term deposit, showing that customer characteristics and past interactions strongly influence the success of marketing efforts.

Class imbalance: The dataset is highly imbalanced, with approximately 11-12% of customers subscribing to a term deposit, suggesting a need for techniques to address this imbalance.

Principal Component Analysis (PCA):

PCA was applied to reduce the dimensionality of the data, but only a low explained variance was achieved with just two principal components.

While there was some separation based on the target variable (subscription status), the reduction did not fully capture all the patterns in the data, suggesting that more complex models might be needed.

Clustering:

K-Means Clustering:

K-Means clustering with k=4 was performed, but the silhouette score was relatively low (around 0.10), indicating poor separation between the clusters.

Clusters such as high-balance, low-engagement customers were identified, but the clustering did not provide clear, meaningful segments that could be used effectively for targeted marketing.

Agglomerative Clustering (N=4):

Agglomerative Clustering with N=4 clusters was applied as an alternative to K-Means. This hierarchical clustering technique does not require the number of clusters to be predefined, but N=4 was specified based on the dendrogram and evaluation of cluster quality.

A dendrogram was generated to visualize the hierarchical relationships between customers, and the optimal cut-off was chosen based on the visual analysis to form 4 clusters.

The silhouette score for Agglomerative Clustering with N=4 was calculated and found to be higher than K-Means, indicating that the hierarchical clustering provided better separation of customer segments.

Profiles of clusters, such as high-balance, high-engagement customers versus low-balance, low-engagement customers, provided deeper insights into customer behavior, showing that Agglomerative Clustering could better capture complex patterns in the data.

Model Performance:

Random Forest and XGBoost both achieved high accuracy (~90%), but their ability to correctly identify subscribed customers was limited by class imbalance.

Precision and recall for the positive class (subscribed customers) were lower, indicating that while the models were able to correctly classify many non-subscribed customers, they struggled with predicting the minority class (subscribed).

XGBoost outperformed Random Forest in most performance metrics, including F1-score, precision, recall, and ROC-AUC.

Feature importance analysis revealed that previous campaign outcome, contact duration, and balance were the most influential features for predicting customer subscription behavior.

---


