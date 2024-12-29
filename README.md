# Analyzing and Predicting Car Prices in the Australian Market

## DataBase - CarPrice
/kaggle/input/carprice/CarPrice.csv
[Kagle Link](https://www.kaggle.com/datasets/lainguyn123/australia-car-market-data/data)

## 1. Overview of Project
- **Objective**:  
  Analyze the Australian Car Market dataset to explore insights and build predictive models. The goal is to identify factors influencing car pricing, discover trends and groupings, and recommend the best model for predicting car prices.  

- **Dataset Details**:  
  The dataset includes attributes such as car price, brand, model, year, mileage, engine capacity, fuel type, gearbox type, and car condition.  

- **Key Questions**:  
  - What factors most influence car prices?  
  - Can we predict car prices using regression models?  
  - Are there specific clusters of cars based on attributes like mileage, engine capacity, or fuel type?    

---

## 2. Exploratory Data Analysis (EDA)
Conduct a thorough analysis to uncover patterns and relationships in the data:  

- **Data Cleaning**:  
  - Handle missing or incorrect values (e.g., null mileage, engine capacity, or outliers in price).  
  - Remove or cap outliers (e.g., extremely high or low prices or mileage).  
  - Check for duplicate records and remove them if necessary.  

- **Feature Transformation**:  
  - Convert categorical variables (e.g., **Brand**, **Fuel**, **Gearbox**) into dummy/encoded variables.  
  - Scale numerical features (e.g., **Kilometers**, **CC**) using Min-Max or StandardScaler for clustering models.  

- **Descriptive Statistics**:  
  - Summary statistics for numerical features (mean, median, range, standard deviation).  
  - Frequency counts for categorical features (e.g., number of cars by brand, fuel type).  

- **Visualization**:  
  - Boxplots to identify outliers in **Price** and **Kilometers**.  
  - Heatmap of correlations to explore relationships between numerical variables like **Year**, **CC**, and **Price**.  
  - Scatterplots (e.g., **Year vs. Price**, **Kilometers vs. Price**) to visualize trends.  

- **Insights**:  
  - Which features have the strongest correlation with car price?  
  - Any notable trends (e.g., newer cars costing more, higher mileage lowering price)?  

---

## 3. Models

## 3.1. Model 1: Clustering
1. **Objective**:  
   Group cars based on similar attributes to identify distinct segments.  

2. **Features for Clustering**:  
   - Select relevant features: **Kilometers**, **CC**, **Year**, **Price**, and **Fuel**.  
   - Normalize the features to ensure equal weight in clustering.  

3. **Clustering Algorithm**:  
   - Use **K-Means Clustering**:  
     - Determine the optimal number of clusters (*k*) using the Elbow Method.  
   - Alternative: **DBSCAN** for density-based clustering.  

4. **Output**:  
   - Visualize clusters with scatter plots (e.g., **Kilometers vs. Price**).  
   - Analyze cluster characteristics (e.g., economy cars vs. luxury cars).  

5. **Insights**:  
   - How do clusters align with pricing and features?  
   - What actionable insights can dealerships derive from these segments?  

---

## 3.2. Model 2: Regression
1. **Objective**:  
   Predict car prices based on features.  

2. **Features for Regression**:  
   - Use features such as **Year**, **Kilometers**, **CC**, **Fuel**, **Gearbox**, **Type**, and **Status**.  

3. **Regression Algorithms**:  
   - **Linear Regression** as a baseline model.  
   - **Random Forest Regressor** or **Gradient Boosting (XGBoost)** for non-linear relationships.  

4. **Train-Test Split**:  
   - Split the dataset into training and testing sets (e.g., 80-20 split).  

5. **Evaluation**:  
   - Metrics: Use **R²**, **Mean Absolute Error (MAE)**, and **Mean Squared Error (MSE)**.  
   - Cross-validate to ensure robustness.  

6. **Feature Importance**:  
   - Identify which features have the greatest impact on car prices.  

---

## 3.3. Optional Additional Model: Classification
- **Objective**:  
  Classify cars into price ranges (e.g., low, medium, high).  

- **Method**:  
  - Use Decision Trees or Naïve Bayes for classification.  
  - Evaluate accuracy, precision, and recall metrics.  

- **Insights**:  
  - Help categorize cars into meaningful price ranges for marketing strategies.  

---

## 4. Best Model
- **Clustering**:  
  - Present cluster visualizations and explain characteristics.  
  - Provide insights into how clusters can help in decision-making (e.g., targeting different customer segments).  

- **Regression**:  
  - Report evaluation metrics for all regression models.  
  - Compare models and choose the best-performing one (e.g., Random Forest for non-linear data).  
  - Discuss why the selected model performs better (e.g., it captures non-linear relationships, handles categorical features well).  

---

## 5. Learning / Challenges
Reflect on your experience:  

- **Learning**:  
  - Gained insights into data preparation and visualization.  
  - Learned how different models behave and their strengths/weaknesses for clustering and regression tasks.  
  - Improved skills in handling categorical data, scaling, and feature selection.  

- **Challenges**:  
  - Handling missing data or outliers in features like **Kilometers** and **Price**.  
  - Balancing model complexity and interpretability.  
  - Computational time for training advanced models like **Gradient Boosting** on large datasets.  

---

## 6. Final Deliverables
- **Code/Notebook**:  
  - A Python notebook with detailed steps for EDA, Clustering, and Regression, including visualizations and insights.  
