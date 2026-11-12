
# Glucose Time-Series Analysis: Forecasting and Deep Learning Classification

## Overview

This project explores two complementary approaches to glucose monitoring data analysis:

1. **Glucose Forecasting:** Time-series modeling to predict future glucose levels using statistical and deep learning approaches.
2. **Glucose Classification:** Transformation of glucose time series into time-frequency scalograms, followed by deep learning-based classification using transfer learning.

The project was developed during an AI/ML research internship at the **Advanced Technologies Development Center (CDTA), Algeria**, from July to September 2024.

---

## Part 1 – Glucose Time-Series Forecasting

### Objective

Analyze continuous glucose monitoring data and develop predictive models to forecast future glucose levels from historical measurements.

### Methodology

**1. Data Exploration and Preprocessing**
- Glucose time-series visualization and statistical analysis.
- Missing value handling and outlier detection using the IQR method.
- Temporal train/test splitting.
- Stationarity analysis using the Augmented Dickey-Fuller (ADF) test.
- Autocorrelation analysis using ACF and PACF plots.

**2. Statistical Forecasting**
- ARIMA model development and parameter selection.
- SARIMA modeling using seasonal components.
- Model evaluation using MAE, MSE, RMSE and R².

**3. Deep Learning Forecasting**
- LSTM (Long Short-Term Memory).
- GRU (Gated Recurrent Unit).
- Sliding-window time-series preparation.
- Training, validation and testing.
- Multi-step future glucose prediction.

Different input window sizes were investigated to study forecasting performance at different temporal contexts.

---

## Part 2 – Glucose Signal Classification Using Deep Learning

### Objective

Investigate the classification of glucose signal patterns by converting one-dimensional glucose time series into two-dimensional time-frequency representations.

### Methodology

**1. Signal Representation**
- Selection and preparation of glucose time-series samples.
- Continuous Wavelet Transform (CWT).
- Generation of 2D scalograms using:
  - Morlet (MORL)
  - Complex Morlet (CMOR)
  - Mexican Hat (MEXH)

**2. Dataset Preparation**
- Organization of scalograms according to their corresponding classes.
- Training/testing split (80/20).
- Image resizing and pixel normalization.
- Data augmentation during training.

**3. Deep Learning Classification**
- VGG16 pretrained on ImageNet.
- Transfer learning with frozen convolutional layers.
- Custom classification layers with Dense and Dropout.
- Multi-class and binary classification experiments.

**4. Model Evaluation**
- Accuracy.
- Precision, Recall and F1-score.
- Confusion matrix.
- Comparison of different wavelet representations and classification settings.

### Results

The binary classification experiment distinguishing Class 1 from Class 4 achieved:

- **93% macro F1-score**

---

## Technologies

- **Programming:** Python
- **Time Series Analysis:** Pandas, NumPy, Statsmodels
- **Statistical Models:** ARIMA, SARIMA
- **Deep Learning:** TensorFlow, Keras
- **Neural Networks:** LSTM, GRU, VGG16
- **Signal Processing:** PyWavelets, Continuous Wavelet Transform
- **Evaluation:** Scikit-learn
- **Visualization:** Matplotlib, Seaborn

---

## Context

Developed during an AI/ML research internship at the **Advanced Technologies Development Center (CDTA), Algeria**, July–September 2024.
