# Results and Model Evaluation

## Project Overview

This project forecasts India's future energy consumption using historical annual data from 1965 to 2023. An LSTM (Long Short-Term Memory) neural network is trained to learn patterns from previous years and predict subsequent values.

## Model Evaluation

The model is evaluated using the following metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Measures prediction error while penalizing larger errors more heavily.

Lower MAE and RMSE values generally indicate better performance when models are evaluated on the same test data and measurement scale.

## Results

Record the results from your latest notebook execution below.

| Evaluation Metric | Result |
|---|---|
| MAE | Add your actual test MAE |
| RMSE | Add your actual test RMSE |
| Baseline MAE | Add your baseline MAE |
| Baseline RMSE | Add your baseline RMSE |

**Important:** Report the final metrics in the original energy-consumption units whenever possible. Do not report scaled metrics as though they were in the original units.

## Actual vs. Predicted Values

The notebook generates a graph comparing actual energy consumption with the values predicted by the LSTM model on the test period. This helps visualize how closely the predictions follow the observed trend.

## Future Forecast

The notebook also generates a forecast for the next year after the latest available observation. The predicted value is an estimate based on historical patterns, not a guaranteed outcome.

## Data Augmentation

Because the available annual observations for India are limited, the project experiments with synthetic training examples created by adding small amounts of random noise to training sequences.

These augmented examples are artificial variations, not additional real-world observations. The test data remains separate from augmentation so that evaluation is based on unseen historical observations.

## Limitations

- The dataset contains a limited number of annual observations for India.
- The model may not capture sudden changes caused by economic conditions, policy decisions, population growth, or technological developments.
- Forecast reliability may decrease when predicting further into the future.
- Synthetic augmentation does not replace collecting more real historical data.
- Model performance should be compared with a simple baseline before concluding that LSTM provides an improvement.

## How to Reproduce the Results

1. Open the project notebook in Google Colab.
2. Upload the original World Energy Consumption CSV file from Kaggle.
3. Run all notebook cells in order.
4. Review the evaluation metrics and actual-versus-predicted graph.
5. Update the results table in this README with the metrics from your latest run.

## Dataset Source

Kaggle — [World Energy Consumption](https://www.kaggle.com/datasets/patricklford/world-energy-consumption)

## Conclusion

This project demonstrates how an LSTM neural network can be applied to time-series forecasting of India's energy consumption. Its usefulness is assessed using MAE, RMSE, a baseline comparison, and a visual comparison of actual and predicted values.
