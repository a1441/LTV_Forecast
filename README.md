# Revenue Prediction Model

This repository contains a Python script designed for modeling user revenue prediction using logarithmic extrapolation.

## Overview

The `LogExtrapolator` class offers functionality to:
- Load historical revenue progression data.
- Fit a logarithmic model to the data.
- Forecast revenue values for a given day.
- Plot actual vs. forecasted revenue data.
- Calculate the Mean Absolute Percent Error between actual and forecasted values.

## Usage

To use the model:

1. **Initialize the model:**

model = LogExtrapolator(prediction_day=90)

2. **Train the model and get predictions:**

df_with_predictions = model.fit_predict(df.drop(columns=['revenue_d90', 'revenue_d120', 'revenue_d180']))

3. **Check for any warnings during the fitting process:**

print("Rows that produced warnings:", model.rows_with_warnings)

4. **Plot the actual vs. predicted revenue:**

![image](https://github.com/a1441/LTV_Forecast/assets/49153959/89cdfeab-4af5-4106-9cf3-bc7e282a69f9)


## Dependencies

- pandas
- numpy
- scipy
- matplotlib

## License

This project is licensed under the MIT License. See the LICENSE file for details.

