# **K-Nearest Neighbors (KNN) Classification Analysis**  
**KNN Model Evaluation and Decision Boundary Visualization**  
**Mini Project**  

## **Overview**  
This project implements **K-Nearest Neighbors (KNN)** classification for a **two-class classification problem** using **both Python and R**. It involves:  

- Training KNN models for \( K = 1,2,3,4,5, \dots, 100 \).  
- Plotting **training and test error rates**.  
- Determining the **optimal \( K \)** based on test error rates.  
- Visualizing the **decision boundary** for the optimal \( K \).  
- **Comparing results between Python and R implementations**.  

---

## **Dataset Description**  

The dataset consists of two files:  
- **`1-training_data.csv`** – Used to train the KNN model.  
- **`1-test_data.csv`** – Used to evaluate model performance.  

Each row represents an **observation with multiple numerical features** and a **binary class label (`Yes` or `No`)**, indicating the classification outcome.  

The goal of this project is to build a **KNN model** that accurately predicts the class label based on input features. The dataset allows us to analyze **error rates across different values of \( K \)** and determine the best trade-off between **bias and variance**.  

---

## **Getting Started**  

### **Prerequisites**  

To run the code, ensure you have the following installed:  

#### **Python Requirements**  
- **Python 3.x**  
- Libraries: `numpy`, `pandas`, `matplotlib`, `scikit-learn`  

#### **R Requirements**  
- **R (version 4.x recommended)**  
- Libraries: `ggplot2`, `class`  

---

## **Results & Analysis**  

### **1. Training & Test Error Trends**  
- The **training error rate** is lowest for \( K=1 \), indicating **overfitting**.  
- The **test error rate** follows a **U-shape**, initially decreasing but later stabilizing or increasing.  

### **2. Optimal \( K \) Selection**  
- The best \( K \) is chosen based on the **minimum test error**.  
- **Optimal \( K \):**  
  - **Python:** \( K=64 \) → **Training Error:** 0.1790, **Test Error:** 0.1780  
  - **R:** \( K=65 \) → **Training Error:** 0.18805, **Test Error:** 0.1785  

### **3. Decision Boundary Visualization**  
- The **decision boundary in Python (K=64)** is **smoother and more generalized**, allowing for better model flexibility.  
- The **decision boundary in R (K=65)** is **more jagged**, showing **higher sensitivity to data points**.  
- Both boundaries **reflect some misclassifications**, especially in overlapping regions, which aligns with expected KNN behavior.  

---

## **Python vs R Comparison**  

This project also includes a **detailed comparison of the results between Python and R**.  

| **Aspect**             | **Python (K=64)**       | **R (K=65)**         |
|------------------------|------------------------|----------------------|
| **Training Error**     | **0.1790**              | **0.18805**         |
| **Test Error**        | **0.1780**              | **0.1785**          |
| **Decision Boundary**  | **Smoother, generalized** | **More jagged, sensitive** |
| **Test Error Trend**   | **Stable at higher K**  | **More variable at low K** |
| **Potential Differences** | **Data splitting, scaling, algorithm implementation** | **Slight variations in classification patterns** |

### **Observations**
- **Both Python and R show similar trends:**  
  - **Low training error at \( K=1 \)**, increasing as \( K \) rises.  
  - **Test error decreases initially, then stabilizes.**  
- **R has slightly more variation in test error at low \( K \)**.  
- **Differences in decision boundary smoothness** suggest variations in how KNN is implemented in Python vs. R.  

For more details, refer to:  
📄 **Results Comparison Python vs R **  