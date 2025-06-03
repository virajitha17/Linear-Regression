# Chicago Taxi Fare Prediction using Linear Regression

This project demonstrates a simple linear regression model built in Google Colab using TensorFlow/Keras to predict taxi fares in Chicago based on trip distance and duration.

## Project Overview

The goal of this project is to explore the relationship between taxi trip attributes (like distance and duration) and the fare charged. A linear regression model is trained to predict the `FARE` based on the `TRIP_MILES` and `TRIP_MINUTES`.

The project involves the following steps:

1.  Loading and exploring the Chicago Taxi Dataset.
2.  Data preprocessing and feature engineering (creating `TRIP_MINUTES` from `TRIP_SECONDS`).
3.  Building and training a linear regression model using Keras.
4.  Visualizing the model's performance and loss curve.
5.  Making predictions on new data and evaluating the model's accuracy using metrics like RMSE, MAE, and R-squared.

## Dataset

The dataset used is the Chicago Taxi Dataset provided by Google, available at: `https://download.mlcc.google.com/mledu-datasets/chicago_taxi_train.csv`.

The key columns used in this project are:

*   `TRIP_MILES`: The distance of the taxi trip in miles.
*   `TRIP_SECONDS`: The duration of the taxi trip in seconds.
*   `FARE`: The final fare of the trip.
*   `COMPANY`: The taxi company.
*   `PAYMENT_TYPE`: The method of payment used.
*   `TIP_RATE`: The tip percentage.

## Requirements

The following libraries are required to run the notebook:

*   `keras`
*   `matplotlib`
*   `numpy`
*   `pandas`
*   `tensorflow`
*   `plotly`
*   `seaborn`
*   `sklearn`

These dependencies are installed within the notebook itself.

## How to View and Run the Notebook

You can view the notebook directly on GitHub, which renders `.ipynb` files.

To run the notebook:

1.  Clone this repository to your local machine or download the `.ipynb` file.
2.  Upload the `.ipynb` file to Google Colab.
3.  Run the cells sequentially.

Alternatively, you can open the notebook directly in Google Colab from GitHub by using the "Open in Colab" button if available, or by going to `File > Open notebook` in Colab and pasting the GitHub URL of the notebook.

## Model Details

A simple linear regression model is built using the Keras Sequential API with a single Dense layer. The model is trained using the Root Mean Squared Error (RMSE) as the loss function and the RMSprop optimizer.

The final model predicts `FARE` based on the linear combination of `TRIP_MILES` and `TRIP_MINUTES`:

`FARE = (weight_for_TRIP_MILES * TRIP_MILES) + (weight_for_TRIP_MINUTES * TRIP_MINUTES) + bias`

## Results and Evaluation

The notebook includes code to train the model, visualize the training process, and evaluate the model's performance on a sample of the data. The evaluation metrics calculated are:

*   Root Mean Squared Error (RMSE)
*   Mean Absolute Error (MAE)
*   R-squared (R2)
*   Mean Absolute Percentage Error (MAPE)

The notebook output will show the values of the learned weights, bias, and these evaluation metrics, providing insights into how well the model predicts taxi fares.

## Conclusion

This project provides a basic example of applying linear regression to predict taxi fares. The results demonstrate the relationship between trip characteristics and fare, and the model provides a reasonable baseline for prediction. Further improvements could involve feature engineering, exploring other regression algorithms, or using more advanced techniques.
