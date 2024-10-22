# Customer Churn Prediction

### Project Overview:
Customer churn is a critical concern for businesses, especially in the telecommunications industry. This project aims to develop a **machine learning-based prediction system** to identify customers who are likely to churn. By accurately predicting customer churn, businesses can proactively implement retention strategies, thereby reducing customer loss and increasing revenue.

### Key Objectives:
1. **Predict Customer Churn**: Build a model that accurately predicts whether a customer will churn based on historical data.
2. **Feature Importance**: Understand which customer attributes (e.g., age, subscription length, monthly bill) are most indicative of churn.
3. **Optimize Model Performance**: Compare multiple machine learning algorithms to find the best model for predicting churn with high accuracy and minimal overfitting.

---

### Dataset:
The dataset contains customer information, including demographic data, subscription details, usage patterns, and a churn label indicating whether the customer has left. Key features include:
- **CustomerID**: Unique identifier for each customer.
- **Age**: Age of the customer.
- **Gender**: Gender of the customer (Male or Female).
- **Location**: Geographical location (Houston, Los Angeles, etc.).
- **Subscription Length**: Number of months the customer has been subscribed.
- **Monthly Bill**: Monthly bill amount.
- **Total Usage (GB)**: Total usage of the service in gigabytes.
- **Churn**: Whether the customer has churned (1) or not (0).

---

### Approach:

1. **Data Preprocessing**:
   - Removed irrelevant columns like `CustomerID` and `Name`.
   - Handled missing values, verified data types, and ensured no duplicate entries.
   - Scaled continuous features such as `Age`, `Subscription Length`, `Monthly Bill`, and `Total Usage GB` using MinMaxScaler to bring them to a common scale.
   - Categorical variables such as `Gender` and `Location` were one-hot encoded.

2. **Exploratory Data Analysis (EDA)**:
   - **Statistical Summary**: Described the distribution of numerical variables (e.g., average customer age of 44 years).
   - **Correlation Analysis**: Checked for correlations between variables using heatmaps. No strong correlations were found between age, usage, or monthly bill and churn.
   - **Class Imbalance**: The dataset was relatively balanced, with approximately 50% churn and 50% non-churn customers.

3. **Feature Selection**:
   - Applied **Random Forest** for feature importance.
   - The four most important features were identified as:
     1. Monthly Bill
     2. Total Usage (GB)
     3. Age
     4. Subscription Length (Months)

4. **Model Building**:
   - Trained multiple machine learning models, including:
     - Logistic Regression
     - Decision Tree
     - Random Forest
     - K-Nearest Neighbors (KNN)
     - Gradient Boosting
     - XGBoost
     - Support Vector Machine (SVM)
     - Neural Networks
   - Evaluated models based on accuracy, precision, recall, F1-score, and training time.
   - Addressed overfitting by using techniques like cross-validation and feature reduction.
   - **Neural Networks** were introduced to improve prediction results.

---

### Key Results:
- **Random Forest and Decision Tree**: Achieved perfect accuracy on training data, indicating potential overfitting.
- **Logistic Regression, KNN, and XGBoost**: Showed moderate performance.
- **Neural Network**: Implemented with early stopping and model checkpointing to improve accuracy while avoiding overfitting.

### Visualizations:
- **Correlation Heatmaps**: Showcased the relationships between variables.
- **Class Distribution**: Illustrated balanced churn distribution.
- **Feature Importance Plot**: Highlighted the importance of different features in predicting churn.
  
---

### Conclusion:
The **Random Forest** model demonstrated the highest accuracy in training, but care was taken to prevent overfitting. A refined **Neural Network** architecture was introduced to further improve model performance. This project serves as a powerful tool for predicting customer churn and offers businesses actionable insights to implement effective customer retention strategies.

### Future Work:
- Fine-tune the **Neural Network** model for even better results.
- Implement advanced techniques such as **ensemble learning** and **hyperparameter tuning**.
- Consider business-specific features that might further enhance prediction accuracy.
