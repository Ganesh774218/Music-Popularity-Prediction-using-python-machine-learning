### **Music Popularity Prediction Report**



#### **Project Overview**



The Music Popularity Prediction project aims to predict how popular a song will be based on various musical and metadata features. Using machine learning techniques, the goal is to model the relationship between song characteristics (like danceability, energy, tempo, etc.) and the popularity score to assist music producers, analysts, and streaming platforms in identifying potential hits.





#### **Objective**



To build a predictive model capable of estimating a song’s popularity score based on audio and descriptive features provided in a dataset.



#### 

#### **Data Preprocessing**



* Several preprocessing steps were applied to clean and prepare the data for modeling:
* Handling Missing Values: Missing values were identified and imputed appropriately.
* Encoding Categorical Variables: String values like genres or artist names were encoded.
* Feature Scaling: Standardization/Normalization was applied to numerical features for uniformity.
* Outlier Detection: Checked for and mitigated outliers that could distort model learning.
* Train-Test Split: Dataset divided into training (80%) and testing (20%) sets for validation.



* I implemented a reproducible preprocessing pipeline: missing values were imputed (median/KNN for numerics, mode or “unknown” for categoricals), categorical/text features were encoded based on cardinality (one‑hot, frequency/target encoding, or embeddings), numeric features were scaled, and outliers were treated (IQR/z‑score capping or isolation‑forest). The data were split 80/20 (stratified when needed) and all transformations were encapsulated in a pipeline fitted on the training set for safe reuse in production.







#### **Model Building**



Multiple machine learning models were trained and compared, including:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor



The Random Forest Regressor provided the most accurate and stable predictions among all models, effectively capturing nonlinear patterns in the data.







#### **Model Evaluation**

Performance Metrics

The following metrics were used to evaluate model performance:

* R² Score (Coefficient of Determination): Measures how well the model explains variance.
* Mean Absolute Error (MAE): Average magnitude of prediction errors.
* Root Mean Squared Error (RMSE): Penalizes larger errors more strongly.



| Model             | R² Score | MAE      | RMSE     |

| ----------------- | -------- | -------- | -------- |

| Linear Regression | Moderate | Medium   | Medium   |

| Decision Tree     | Improved | Moderate | Moderate |

| \*\*Random Forest\*\* | \*\*High\*\* | \*\*Low\*\*  | \*\*Low\*\*  |







#### **Visualization \& Analysis**



The following visualizations were created to analyze results:

* Feature Correlation Heatmap: Displays relationships between numerical variables.
* Distribution Plots: Show how each feature varies across the dataset.
* Predicted vs. Actual Popularity Plot

As shown in your attached graph, the green line (actual) and orange line (predicted) closely follow each other, confirming that the Random Forest model effectively predicts popularity trends with minimal error.







#### **Key Insights**

* Songs with higher energy, valence, and danceability tend to have higher popularity.
* Acoustic tracks generally have lower popularity scores compared to more energetic or upbeat ones.
* Random Forest performed best because it handled nonlinear relationships and feature interactions effectively







##### **Conclusion**

* The project produced a reliable predictive pipeline for estimating song popularity from audio features and metadata, with the Random Forest Regressor delivering the strongest and most consistent performance across validation tests.
* Its robustness and ability to capture non-linear relationships made it effective at modeling complex interactions between features such as energy, danceability, and acousticness.
* Beyond accuracy, the model’s feature-importance insights provide actionable guidance for artists, labels, and marketers to prioritize musical and promotional levers.0
* For practical adoption, next steps include enriching the feature set (promotion and playlist data), evaluating ensemble or calibrated models, and validating performance in A/B tests or live deployment to ensure sustained predictive validity.
