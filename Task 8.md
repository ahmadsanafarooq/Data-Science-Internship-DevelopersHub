# **Loan Default Risk Prediction - Performance Report**  

## **📌 Objective**  
The objective of this project is to develop a machine learning model that accurately predicts **loan default risk** based on financial and demographic factors. The goal is to assist lenders in making informed decisions when approving loans, reducing financial risks while ensuring responsible lending.  

---

## **📊 Methodology**  

### **1️⃣ Data Loading and Preprocessing**  
✔ Loaded the loan default risk dataset.  
✔ Handled missing values by **imputing the mean** for 'Debt_Amount' and 'Monthly_Savings'.  
✔ Removed duplicate records to ensure data integrity.  

### **2️⃣ Exploratory Data Analysis (EDA)**  
✔ **Visualized distributions** of 'Retirement_Age', 'Debt_Amount', and 'Monthly_Savings' using histograms.  
✔ **Checked feature correlations** using a heatmap to identify significant relationships.  
✔ **Detected outliers** in 'Retirement_Age' and 'Debt_Amount' using boxplots.  
✔ **Explored relationships** between features and loan default risk using boxplots.  
✔ **Applied log transformation** to 'Debt_Amount' to reduce skewness.  

### **3️⃣ Feature Scaling**  
✔ Standardized numerical features ('Debt_Amount', 'Monthly_Savings', 'Retirement_Age') using **StandardScaler**.  

### **4️⃣ Data Splitting and Balancing**  
✔ Split dataset into **80% training and 20% testing sets**.  
✔ Addressed class imbalance by **applying SMOTE** (Synthetic Minority Over-sampling Technique).  

### **5️⃣ Model Training and Evaluation**  
✔ **Trained an SVM (Support Vector Machine) classifier** using an **RBF kernel**.  
✔ Evaluated performance using:  
   - **Accuracy**  
   - **Classification Report** (Precision, Recall, F1-score)  
   - **Confusion Matrix**  

---

## **🔍 Results**  

✅ **Model Accuracy:** **0.95 (95%)** on the test dataset.  
✅ **Classification Report:**  
   - The model achieved **high precision and recall**, ensuring accurate loan default predictions.  
✅ **Confusion Matrix:**  
   - The confusion matrix showed **minimal false positives and false negatives**, demonstrating strong predictive performance.  

---

## **💡 Recommendations for Lenders**  

### **1️⃣ Implement the Model**  
- Integrate the **trained SVM model** into the loan approval process to assess the risk of **loan default** before approving applications.  

### **2️⃣ Focus on Key Features**  
- Based on EDA findings, **'Debt_Amount' and 'Retirement_Age'** significantly impact default risk.  
- Lenders should **closely evaluate applicants with high debt levels or early retirement ages**.  

### **3️⃣ Adjust Decision Thresholds**  
- Depending on **risk tolerance**, the threshold for classifying applicants as **high risk** can be adjusted.  

### **4️⃣ Continuous Monitoring & Updating**  
- **Retrain the model regularly** on new loan application data to **maintain high accuracy**.  
- Update features and retrain when economic conditions and borrower behaviors change.  

### **5️⃣ Consider Adding More Features**  
- Future versions of the model can include additional data such as:  
  - **Credit history**  
  - **Income levels**  
  - **Employment stability**  
  - **Past loan repayment behavior** 
