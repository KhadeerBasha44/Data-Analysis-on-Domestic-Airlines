
# **Data Analysis on Domestic Airlines in India**  
*A Predictive Modeling Project for Passenger Traffic and Customer Satisfaction*  


## **📌 Overview**  
This project combines **time-series forecasting** and **machine learning** to analyze India’s domestic aviation sector. It aims to:  
1. **Predict passenger traffic** using SARIMA (Seasonal ARIMA).  
2. **Forecast customer satisfaction** using a Random Forest classifier.  
3. **Provide actionable insights** to improve airline operations and passenger experience.  

---

## **📂 Datasets Used**  
1. **Passenger Traffic Data**  
   - **Source**: [Directorate General of Civil Aviation (DGCA), India](https://www.dgca.gov.in/digigov-portal/?page=259/4184/servicename)  
   - **Time Period**: Jan 2012 – Dec 2022  
   - **Features**: Monthly passenger counts, payload, resource allocation.  

2. **Customer Satisfaction Data**  
   - **Source**: [Kaggle (Airline Passenger Satisfaction)](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction?datasetId=522275)  
   - **Size**: 20,000+ survey responses  
   - **Features**: In-flight amenities, delays, booking experience, satisfaction labels (satisfied/neutral/dissatisfied).  

---

## **⚙️ Methodology**  

### **1. SARIMA Model (Time-Series Forecasting)**  
- **Goal**: Predict future passenger demand.  
- **Steps**:  
  - Data differencing for stationarity.  
  - Seasonal decomposition (period=6 months).  
  - ACF/PACF analysis for parameter tuning.  
  - Model evaluation using RMSE.  

### **2. Random Forest Classifier (Machine Learning)**  
- **Goal**: Predict passenger satisfaction.  
- **Steps**:  
  - Handling missing values (e.g., filling `Arrival Delay` NaNs with 0).  
  - Feature engineering (label encoding, correlation analysis).  
  - Model training with hyperparameter tuning (`max_depth=25`, `n_estimators=100`).  
  - Evaluation metrics: ROC-AUC, accuracy, and confusion matrix.  

---

## **📊 Key Results**  

### **SARIMA Model**  
- Forecasted passenger growth trends for 2023–2032.  
- Identified seasonal peaks (e.g., holiday travel surges).  

### **Random Forest Model**  
- **Top influential features**:  
  1. Online boarding experience  
  2. In-flight WiFi service  
  3. Departure/arrival delays  
- **Accuracy**: ~92% (on test data).  

---

## **🚀 How to Run the Code**  

### **Prerequisites**  
- Python 3.8+  
- Libraries: `pandas`, `numpy`, `statsmodels`, `scikit-learn`, `matplotlib`, `seaborn`  

### **Steps**  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/khadeerbasha44/domestic-airlines-analysis.git  
   cd domestic-airlines-analysis  
   ```  

2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. Run the Jupyter notebooks:  
   - `SARIMA_Passenger_Forecasting.ipynb`  
   - `RandomForest_Customer_Satisfaction.ipynb`  

---

## **📝 Conclusion & Recommendations**  
- **Passenger traffic** is expected to grow significantly (SARIMA forecasts).  
- **Customer satisfaction** can be improved by focusing on:  
  - Reducing flight delays.  
  - Enhancing in-flight WiFi and entertainment.  
  - Streamlining online boarding processes.  

---

## **📜 License**  
This project is open-source under the **MIT License**.  

---

## **✉️ Contact**    
- **Email**: [khadeershaik2906@gmail.com]  

---

### **🔗 Useful Links**  
- [DGCA Data Portal](https://www.dgca.gov.in)  
- [Kaggle Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)  

---
