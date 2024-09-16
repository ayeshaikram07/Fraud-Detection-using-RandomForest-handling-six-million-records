# Fraud-Detection-using-RandomForest-handling-six-million-records
Designed and implemented a RandomForest-based fraud detection model, leveraging SMOTE for imbalanced data handling and optimized via RandomizedSearchCV, achieving high precision and effective fraud detection in financial transactions

note:dataset is too large it cannot import in the github ...
### 1. **Data Cleaning:**
   - **Missing Values:** Filled in missing data or removed sparse rows.
   - **Outliers:** Kept outliers, as they could indicate fraud.
   - **Multi-Collinearity:** Checked for highly related features, removing or transforming them as needed to avoid redundancy.

### 2. **Fraud Detection Model (RandomForest):**
   - Used RandomForest because it's good with complex data.
   - To handle the imbalance between fraudulent and non-fraudulent transactions, I used **SMOTE** to generate more fraud samples.
   - I tuned the model using **RandomizedSearchCV** for efficient hyperparameter tuning.
   - Chose **hold-out validation** (splitting data into training and test sets) due to time constraints instead of cross-validation.

### 3. **Variable Selection:**
   - Key variables were:
     - **Transaction amount:** Fraudsters often deal with large sums.
     - **Balance changes:** Sudden drops in balance are suspicious.
     - **Transaction types:** Some types (e.g., CASH-OUT) are riskier.

### 4. **Model Performance:**
   - **Precision:** The model was great at flagging fraud without false alarms.
   - **Recall:** It missed some fraud cases, meaning some went undetected.
   - **Overall:** The model worked well but could improve at catching all fraud.

### 5. **Key Factors Predicting Fraud:**
   - Large transaction amounts, big balance changes, and specific transaction types (like transfers and cash-outs) were key indicators of fraud.

### 6. **Do These Factors Make Sense?**
   - Yes, these are common signs of fraud in financial transactions.

### 7. **Prevention Measures:**
   - Add **real-time monitoring** for suspicious transactions.
   - Set **limits on high-risk transactions**.
   - Use **stronger authentication** for large transfers.

### 8. **Checking if It Works:**
   - Track fraud rates after implementing measures.
   - Regularly check the model's performance.
   - Gather customer feedback to ensure it's not too restrictive.

