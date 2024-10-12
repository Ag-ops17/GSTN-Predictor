# GSTN-Predictor
This project demonstrates a comprehensive machine learning pipeline to predict GSTN (Goods and Services Tax Number) outcomes using a combination of Random Forest and K-Nearest Neighbors (KNN) classifiers. The pipeline includes various stages such as data preprocessing, feature selection, model training, and evaluation.By leveraging advanced techniques such as Gaussian filter addition and power transformation, we achieved highly accurate predictions.

Table of Contents
Folder Structure
Data Preparation
Data Description
Modeling Process
Results
Contributors
Folder Structure


The project directory includes the following structure:

   ├── knn_predictions.csv
   ├── rf_features.csv
   └── rf2_predictions.csv
── Code
   ├── gst_code.py
   └── GSTN_CODE.py
── README.md


Train_60: Contains training data with features (X_Train_Data_Input.csv) and corresponding target labels (Y_Train_Data_Target.csv).
Test_20: Contains test data used to validate model predictions.
Data Description
X_Train_Data_Input.csv: Feature matrix for training. The features may include both numerical and categorical data relevant to the prediction.
Y_Train_Data_Target.csv: Target values (dependent variable) for the training data, which the model will learn to predict.
X_Test_Data_Input.csv: Features for testing the model’s predictive capabilities on unseen data.
Y_Test_Data_Target.csv: True target values for the test set, used for model evaluation.
Modeling Process

Data Loading:
Training and testing datasets are loaded using pandas for further processing.

Data Cleaning:
Irrelevant columns are dropped, and missing values are filled with feature mean or median to maintain data integrity.

Feature Correlation Analysis:
Features are analyzed for correlation with the target variable. Columns with high correlation or potential data leakage are noted for further steps.

Data Scaling:
Feature standardization ensures uniformity across the dataset, and power transformation improves robustness by stabilizing variance.

Model Training:

Random Forest Classifier: The first Random Forest model is trained, and important features are extracted.
KNN Classifier: These features are then fed into a K-Nearest Neighbors (KNN) model to capture local patterns.
Combining Predictions: KNN predictions are combined with Random Forest features for input into the final Random Forest model.
Second Random Forest Classifier: This combined dataset is used to train a second Random Forest model, yielding optimal results.

Results
The final model achieved 100% accuracy by combining Random Forest and KNN methods with advanced preprocessing techniques like Gaussian filter addition and power transformation.
Intermediate models, such as XGBoost (98%), ANN (97%), and Voting Classifiers (96%), provided robust benchmarks but were outperformed by the final hybrid model.


Contributors

Agnimitra Gupta
Email: iamgni45@gmail.com

Arka Ghosh
Email: arkaghosh566@gmail.com

Sayantan Dey
Email: sayantandey0429@gmail.com

Shreya Singh
Email: shreyasingh19092001@gmail.com

Subhangani Jha
Email: subhanganijha@gmail.com
