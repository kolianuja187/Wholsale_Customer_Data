
# **Wholesale Customer Data Clustering – Machine Learning Project Report**

## **1. Introduction**

The **Wholesale Customer Data Clustering App** is an unsupervised machine learning project designed to identify distinct customer segments based on their purchasing behavior. Clustering can help businesses understand their customer base, personalize marketing strategies, and optimize product offerings.

---

## **2. Project Objectives**

* Group wholesale customers into meaningful clusters based on spending behavior.
* Use clustering techniques to uncover hidden patterns in customer data.
* Build a reusable and deployable clustering pipeline.
* Enable businesses to target specific customer groups more effectively.

---

## **3. Project Structure and Files**

| **File Name**                  | **Description**                                                                                       |
| ------------------------------ | ----------------------------------------------------------------------------------------------------- |
| `Wholesale_customer_data.xls`  | Raw dataset containing annual spending data of wholesale customers across various product categories. |
| `Clustering.ipynb`             | Jupyter Notebook used for data preprocessing, visualization, and applying clustering algorithms.      |
| `Wholesale_Customers1 (1).pkl` | Trained clustering model (pipeline) saved using `pickle` for future deployment or analysis.           |

---

## **4. Dataset Overview**

**Source:** UCI Machine Learning Repository – Wholesale Customers Data Set
**Attributes:**

* Channel (Horeca/retail)
* Region
* Fresh
* Milk
* Grocery
* Frozen
* Detergents\_Paper
* Delicassen

These features represent the annual spending on different product categories for each customer.

---

## **5. Data Preprocessing**

**Performed in:** `Clustering.ipynb`

### Key Steps:

* Loaded the Excel dataset and performed initial exploration.
* Checked and handled missing values (none found).
* Scaled numerical features using `StandardScaler` to ensure fair clustering distance metrics.
* Removed outliers using z-score or IQR method for better cluster separation.
* Optional dimensionality reduction using PCA to visualize clusters.

---

## **6. Clustering Techniques Applied**

### Algorithms Tested:

* **K-Means Clustering**
* **Hierarchical Clustering (Agglomerative)**
* **DBSCAN (Density-Based Spatial Clustering)**

### Model Selection:

* **K-Means** was chosen for its interpretability and clear separation of clusters.
* Used **Elbow Method** and **Silhouette Score** to determine optimal number of clusters.

  * Optimal number of clusters found: **3**

---

## **7. Cluster Analysis**

**Performed in:** `Clustering.ipynb`

* Visualized clusters using PCA (2D projection).
* Interpreted each cluster based on average spending patterns.

### Example Cluster Interpretations:

* **Cluster 0:** Small businesses with moderate spending in all categories.
* **Cluster 1:** High-volume customers, major spending in Grocery and Milk.
* **Cluster 2:** Niche customers focused on Fresh and Frozen goods.

---

## **8. Model Saving and Deployment**

* Final clustering model (with preprocessing) was serialized as `Wholesale_Customers1 (1).pkl` using `pickle`.
* The model can now be integrated into dashboards or internal analytics systems to classify new customers.

---

## **9. Results and Insights**

* Clear customer segmentation allows for **targeted marketing** and **inventory planning**.
* Businesses can focus resources on high-value clusters.
* Potential to offer custom discounts or loyalty programs based on cluster membership.

---

## **10. Future Enhancements**

* Integrate with customer CRM systems for real-time clustering.
* Add features such as **customer demographics**, **frequency**, and **recency of purchases**.
* Use **AutoClustering** or **deep clustering** for improved cluster discovery.
* Build a **Streamlit or Flask web app** for interactive use by marketing or sales teams.

---

## **11.Output

<img width="841" height="850" alt="image" src="https://github.com/user-attachments/assets/868fef8f-7d6e-4c32-91dc-71b77fc9af12" />

## **12. Conclusion**

The **Wholesale Customer Data Clustering** project effectively demonstrates the power of unsupervised learning in customer segmentation. The model is lightweight, interpretable, and scalable, making it highly valuable for business intelligence applications in the wholesale sector.


