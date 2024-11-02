# Rainfall Prediction in Australia

This repository contains the group project for **TDS 3851: Machine Learning**. The project investigates the effectiveness of machine learning and deep learning techniques in predicting the amount of rainfall in Australia, with a specific focus on comparing Artificial Neural Network (ANN), Recurrent Neural Network (RNN), and Gated Recurrent Units (GRU) models.

## Project Overview
Rainfall prediction is crucial for various sectors, especially in Australia, where agriculture, water resource management, and disaster prevention are heavily dependent on accurate forecasts. This study aims to predict rainfall amounts by implementing machine learning models and evaluating their performance against existing research.

## Dataset
The dataset used for this project is available on Kaggle, titled ["Rain in Australia"](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package). It contains daily meteorological data from 49 Australian cities over nearly a decade, with 23 features and approximately 145,460 records. The target variable for prediction is the "Rainfall" feature, representing the amount of precipitation expected for the next day.

## Key Steps and Findings
### 1. Data Preprocessing
- **Null Value Handling**: Features with excessive null values were removed, while others were imputed based on seasonal averages.
- **Outlier Removal**: Outliers were handled using the Interquartile Range (IQR) method.
- **Normalization and Encoding**: Standard Scaler normalization was applied, and categorical variables were converted to numeric values.
- **Balancing Data**: Oversampling was used to address class imbalance in "RainToday" and "RainTomorrow".

### 2. Feature Selection
- The **Boruta algorithm** was used to identify key features influencing rainfall, including factors like temperature, humidity, and wind direction.

### 3. Model Training and Evaluation
We trained and compared the following models:
- **Artificial Neural Network (ANN)**
- **Recurrent Neural Network (RNN)**
- **Gated Recurrent Unit (GRU)**

Each model was evaluated based on **Mean Squared Error (MSE)**, **Mean Absolute Error (MAE)**, and **R-Squared (R²)** metrics.

### 4. Hyperparameter Tuning
Hyperparameter tuning was performed using a randomized search approach. The final optimized parameters provided improvements in model performance, particularly for the RNN and GRU models.

## Results
- **RNN and GRU models** outperformed the ANN in terms of predictive accuracy, with GRU achieving the best results (MAE = 0.091, MSE = 0.032, R² = 0.759).
- Compared to a selected research paper using similar techniques, our models showed improved MSE and MAE scores, demonstrating the potential of deep learning for reliable meteorological predictions.

## Conclusion and Future Enhancements
This project demonstrates the capability of neural networks, particularly recurrent models like RNN and GRU, in predicting rainfall amounts. Future work could explore more advanced hyperparameter tuning methods like grid search, additional validation metrics, and ensemble models to further improve accuracy.

## License
This project is for educational purposes as part of coursework for TDS 3851.
