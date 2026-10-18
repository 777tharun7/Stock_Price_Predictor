<div align="center">

# Google Stock Price Forecasting — LSTM Experiment

**Sequence modelling with Keras LSTM layers and scaled historical-price inputs**

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter- F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)

</div>

## Overview

An educational time-series forecasting project using Keras LSTM layers to model historical Google stock-price data. The notebooks demonstrate data loading, scaling, sequence/model training, plotting, and saving model artifacts.

## Implementation found in the repository

- `Stock_Price_Predictor.ipynb` — training and evaluation workflow.
- `Stock_Price_Predictor_stream_lit.ipynb` — a second notebook for the model/demo workflow.
- `Stock_Price_Predictor_model .h5` — saved model artifact (the filename contains a space before `.h5`).

**Stack:** Python · pandas · NumPy · Matplotlib · scikit-learn · TensorFlow/Keras (LSTM, Dense, Dropout)

## Reproducibility status

The notebooks read `google.csv`, but that data file is not currently included in the repository. The notebooks also refer to saved model names that do not clearly match the artifact checked into the repository. Supply a permitted dataset and reconcile the save/load paths before treating the workflow as reproducible.

Dependencies used by the notebook include:

```bash
python -m pip install pandas numpy matplotlib scikit-learn tensorflow
```

Open the notebook in Jupyter or Google Colab, place `google.csv` at the path expected by the code, and run cells in order.

## Evaluation note

A saved notebook output reports train MSE/RMSE of `0.00012338 / 0.01110775` and test MSE/RMSE of `0.00116195 / 0.03408742`. These values are reported on the model's scaled target, not in stock-price currency, and have not been independently rerun during this audit. They should not be presented as real-world forecast accuracy without a documented asset/date range, chronological holdout, inverse-scaled MAE/RMSE, and naive baseline comparison.

## Limitations

Historical-price forecasting is sensitive to period selection, look-ahead leakage, market regime changes, and data adjustments. This experiment is not investment advice and does not establish a profitable trading strategy.

## Files

- [Training notebook](Stock_Price_Predictor.ipynb)
- [Second notebook](Stock_Price_Predictor_stream_lit.ipynb)
- [Repository](https://github.com/777tharun7/Stock_Price_Predictor)
