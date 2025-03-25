# Porter Delivery Time Prediction

This project builds a regression model to predict food delivery times based on real intra-city logistics data from Porter, India’s largest marketplace for intra-city logistics. The goal is to estimate how long a food order will take to be delivered, based on the order details, restaurant type, and availability of delivery partners.

refer blog: [Predicting Delivery Time in Intra-City Logistics Using Neural Networks](https://medium.com/@shivaramcholleti/predicting-delivery-time-in-intra-city-logistics-using-neural-networks-dd7b7ed7147a)

## Dataset

The dataset contains over 190,000 delivery records with features including:

- Timestamps (`created_at`, `actual_delivery_time`)
- Restaurant category and order protocol
- Order size and item prices
- Operational metrics like on-shift and busy delivery partners

## Objective

Predict the delivery time (in minutes) using a neural network, based on historical order and logistics data.

---

## Workflow

### 1. Data Preprocessing
- Parsed datetime features
- Extracted delivery time (target), order hour, and day of the week
- Handled missing values with median imputation and categorical placeholders

### 2. Data Cleaning
- Visualized distributions and detected outliers
- Removed outliers using the IQR method

### 3. Feature Engineering
- One-hot encoding for categorical features
- Standardization of numerical features

### 4. Model Building
- Neural network built using TensorFlow/Keras
- Architecture: 64 → 32 → 1 with ReLU activation
- Trained using Mean Squared Error loss and MAE as an evaluation metric

---

## Evaluation Metrics

The model was evaluated using the following metrics on a test set:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

## Results

MSE: **163.70**
RMSE: **12.79**
MAE: **10.12**
