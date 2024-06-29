# Flight-price-predictor-ML-

### WEB APP LINK -> https://sagemaker-flight-prices-prediction-5yfn7cnnpxta2k23jvf4ic.streamlit.app/

This ML project aims to preprocess flight data, train a machine learning model, and deploy a web application for predicting flight prices.

## Preprocessing Pipelines
- Airline Transformer: Handles missing values, rare labels, and encodes airline data using SimpleImputer, RareLabelEncoder, and OneHotEncoder.
- Date of Journey Transformer: Extracts datetime features and scales them using DatetimeFeatures and MinMaxScaler.
- Location Transformer: Handles rare labels, encodes, scales, and adds a north city indicator using RareLabelEncoder, MeanEncoder, PowerTransformer, and custom functions.
- Time Transformer: Extracts time features, encodes part of the day, and scales them using DatetimeFeatures, FunctionTransformer, CountFrequencyEncoder, and MinMaxScaler.
- Duration Transformer: Transforms duration into various features including RBF similarity, categorizes duration, scales, and handles outliers using custom classes, RBFPercentileSimilarity, and standard preprocessing tools.
- Total Stops Transformer: Adds a direct flight indicator using SimpleImputer and FunctionTransformer.
- Additional Info Transformer: Handles rare labels, encodes, and adds an information indicator using RareLabelEncoder, OneHotEncoder, and FunctionTransformer.
## Column Transformer
- Combines all individual transformers into a single ColumnTransformer.
## Feature Selector
- Uses a RandomForestRegressor to select important features based on R-squared scoring with SelectBySingleFeaturePerformance.
## Preprocessing Pipeline
- Combines the column transformer and feature selector into a preprocessing pipeline.
## Training and Saving the Preprocessor
- Reads training data, fits the preprocessor, and saves it using joblib.
## Streamlit Web Application
- Configures and builds a web application for flight price prediction.
- Accepts user inputs for flight details, preprocesses the inputs, loads the saved preprocessor and model, and displays the predicted price using Streamlit.

### WEB APP LINK -> https://sagemaker-flight-prices-prediction-5yfn7cnnpxta2k23jvf4ic.streamlit.app/





