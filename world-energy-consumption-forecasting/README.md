# World Energy Consumption Forecasting Using LSTM

A beginner-friendly Google Colab project that uses an LSTM neural network to forecast India's annual energy consumption from the previous five years.

## Problem statement
An energy research organization wants to predict a country's future energy consumption using historical yearly records.

## Dataset
Download the World Energy Consumption dataset from Kaggle:
https://www.kaggle.com/datasets/patricklford/world-energy-consumption

The notebook supports a wide-format CSV with one column per year, such as `1965`, `1966`, and so on. Upload the downloaded CSV when prompted.

## Methods
- Select India and clean missing/invalid values
- Sort annual observations chronologically
- Min-Max normalization (scaler fitted on pre-test years)
- Five-year sliding windows to predict the next year
- LSTM model using TensorFlow/Keras
- MAE and RMSE evaluation in original dataset units
- Previous-year baseline comparison
- Actual-versus-predicted plot and one-year-ahead forecast

## Run in Google Colab
1. Open the notebook in `notebooks/world_energy_forecasting.ipynb`.
2. Upload it to Google Colab, or click **Open in Colab** after adding the notebook to GitHub.
3. Run each cell in order.
4. Upload the CSV downloaded from Kaggle when prompted.

## Results
Record the MAE and RMSE printed by the notebook after running it on your own dataset. Do not claim results that have not been reproduced. Metric values depend on the exact data and split.

## Important limitations
- Annual data for a single country is small (around 59 records in the provided dataset).
- Synthetic augmentation creates perturbed training examples; it does not create new real observations.
- A low error is not guaranteed. Compare the LSTM with the included previous-year baseline.
- Use only the test set for final evaluation and report whether errors are on the original or normalized scale.

## Technologies
Python, Pandas, NumPy, Matplotlib, scikit-learn, TensorFlow/Keras, Google Colab.
