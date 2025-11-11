# Music-Popularity-Prediction-using-python-machine-learning

Music Popularity Prediction with python machine learning


Music popularity prediction applies statistical and machine learning regression models to estimate a song’s future audience engagement—streams, downloads, and chart performance—using audio features, metadata, release timing, artist profile, playlist placement, and promotional signals.
Reliable forecasts allow artists, labels, and marketers to prioritize releases, tailor promotional investment, optimize playlist and radio outreach, and forecast revenue, while interpretability of the models reveals which musical and non-musical attributes most strongly influence success.


Overview
This project uses machine learning to forecast a song’s popularity from audio features and metadata—such as danceability, energy, tempo, loudness, genre, and release context—to uncover the musical and contextual attributes that drive audience engagement. The workflow combines exploratory analysis and feature engineering with regression and classification models, along with explainability techniques, to produce robust, interpretable predictions and actionable insights.



Objective
To build a predictive model that classifies whether a song will be popular or not, using a dataset of music features and performance metrics


Dataset

The dataset contains various numerical and categorical features describing songs.
Typical columns include:
⦁	acousticness – How acoustic the track is
⦁	danceability – Suitability for dancing based on rhythm and beat
⦁	energy – Measure of intensity and activity
⦁	liveness – Presence of live audience in the track
⦁	loudness – Average decibel level of the track
⦁	speechiness – Amount of spoken words
⦁	tempo – Speed of the track
⦁	valence – Musical positivity
⦁	duration_ms – Song length in milliseconds
⦁	popularity – Target variable (numeric score or categorical label)



Data Preprocessing

⦁	Missing Values: Handled using imputation or removal of incomplete records.
⦁	Encoding: Categorical features were converted using label encoding or one-hot encoding.
⦁	Scaling: Numerical features were normalized using StandardScaler.
⦁	Outlier Removal: Detected and removed using the Interquartile Range (IQR) method.



Exploratory Data Analysis (EDA)

Performed analysis to uncover patterns such as:
⦁	Correlation between musical attributes and popularity.
⦁	Relationship between tempo, loudness, and energy.
⦁	Distribution of popularity scores across different song features.

Visualization tools like Matplotlib, Seaborn, and Plotly were used to create bar charts, heatmaps, and scatter plots.



Machine Learning Models Used

Several algorithms were applied and compared:
⦁	Random Forest Classifier
⦁	Support Vector Machine (SVM)
⦁	Logistic Regression
⦁	K-Nearest Neighbours (KNN)

Each model was trained and evaluated using:
⦁	Train-Test Split (e.g., 80%-20%)
⦁	Accuracy, Precision, Recall, and F1-Score


Model Evaluation
The Random Forest Classifier provided the best performance due to its robustness in handling both numerical and categorical data, achieving high prediction accuracy on the test set.



Insights
⦁	Songs with high energy, danceability, and positive valence are more likely to be popular.
⦁	Loudness and tempo also showed significant positive correlation with popularity.
⦁	The project highlights how data-driven insights can support artists, producers, and streaming platforms.



Technologies Used
⦁	Python
⦁	Pandas, NumPy
⦁	Scikit-learn
⦁	Matplotlib, Seaborn, Plotly
⦁	Jupyter Notebook


Conclusion
⦁	This project demonstrates how machine learning and data analysis can reveal key factors that contribute to a song’s popularity.
⦁	With continuous improvements, such models can provide valuable insights for music producers, streaming services, and marketing teams.
