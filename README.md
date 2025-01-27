# Customer Segmentation and Lookalike Model

## Overview
This project focuses on two primary tasks:

1. **Customer Segmentation:**
   - Use clustering techniques to group customers based on transactional and demographic data.
   - Provide insights into customer behavior and preferences through visualization and summary statistics.

2. **Lookalike Model:**
   - Identify customers with similar behaviors and preferences using a cosine similarity-based approach.
   - Generate lookalike recommendations for each customer.

Additionally, the project outputs:
- A **Clustering Report (PDF)** containing:
  - Number of clusters
  - Davies-Bouldin Index (DBI)
  - Summary of results
- A **Cluster Assignments (CSV)** listing each customer with their assigned cluster.
- A **Lookalike Recommendations (CSV)** listing top similar customers for each input.

---

## Files and Outputs

### Input Files
1. `Customers.csv`: Contains customer demographic data.
2. `Transactions.csv`: Contains transactional details for each customer.
3. `Products.csv`: Contains product details and their respective categories.

### Output Files
1. **Clustering_Report.pdf**: Summary of the clustering analysis, including DBI and cluster insights.
2. **Cluster_Assignments.csv**: Each customer's cluster assignment.
3. **Lookalike.csv**: Top three lookalike customers for each customer based on cosine similarity.

---

## Code Structure

### 1. Data Loading and Preprocessing
- Mounts Google Drive to access input files and save outputs.
- Loads `Customers.csv`, `Transactions.csv`, and `Products.csv`.
- Performs necessary preprocessing like handling missing values and feature scaling.

### 2. Feature Engineering
- **Customer Features:**
  - Aggregates transactional data to create features like total spending, average spending, and transaction count.
  - Extracts category preferences using pivot tables and normalizes them.
  - Encodes customer region information as one-hot vectors.

### 3. Customer Segmentation
- Implements K-means clustering to group customers.
- Calculates the Davies-Bouldin Index (DBI) to evaluate clustering performance.
- Saves cluster assignments to `Cluster_Assignments.csv`.

### 4. Lookalike Model
- Uses cosine similarity to find top three similar customers for each input customer.
- Outputs recommendations to `Lookalike.csv`.

### 5. Reporting
- Generates a **Clustering_Report.pdf** with:
  - Number of clusters
  - DBI value
  - Key insights and cluster summaries

---

## Instructions to Run

### Requirements
1. Python 3.x
2. Libraries:
   - `pandas`
   - `numpy`
   - `sklearn`
   - `matplotlib`
   - `seaborn`
   - `fpdf`

### Steps
1. **Upload Input Files:**
   - Place `Customers.csv`, `Transactions.csv`, and `Products.csv` in Google Drive.
2. **Run the Script:**
   - Execute the script in Google Colab or a local Jupyter Notebook.
   - Ensure Google Drive is mounted to access input files and save outputs.
3. **View Outputs:**
   - Download `Clustering_Report.pdf`, `Cluster_Assignments.csv`, and `Lookalike.csv` from the specified output directory.

---

## Evaluation Metrics

### 1. Clustering Evaluation
- **Davies-Bouldin Index (DBI):** Lower values indicate better clustering.

### 2. Lookalike Model Evaluation
- **Cosine Similarity:** Measures similarity between customers based on their features.

---

## Recommendations for Improvement
1. **Feature Importance Analysis:** Add SHAP or other techniques to explain clustering and lookalike results.
2. **Validation Metrics:** Incorporate additional metrics like Silhouette Score for clustering validation.
3. **Cluster Profiling:** Provide more detailed analysis of each cluster's demographics and preferences.
4. **Predictive Insights:** Extend business insights with predictive modeling.

---

## Contact
For any questions or feedback, please contact:
- Name: Adinarayana
- Email: thotaadinarayana02@gmail.com


