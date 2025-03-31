# E-Commerce-Purchase-Prediction-System

This repository contains an end-to-end pipeline for processing item and event data, training a predictive model for purchase behavior, and evaluating its performance using visual dashboards.

## Overview

The project consists of three main components:

1. **Data Processing**  
   The `DataProcessor` class loads and preprocesses CSV files containing category trees, item properties, and events. It normalizes features such as price and category IDs and constructs fixed-length sequential data for each visitor.

2. **Model Building & Training**  
   The `EnhancedPredictor` class defines a neural network using Bidirectional LSTM layers with multi-head attention. The model is trained on the sequences produced by the data processor to predict whether a visitor will make a purchase.

3. **Evaluation & Dashboard**  
   The `EnhancedDashboard` class provides real-time visualizations of training metrics (loss, AUC, precision, recall), prediction distributions, and ROC curves. There is also a function to load a saved model and evaluate its performance.

## File Structure

- **`data_processor.py`**: Contains the `DataProcessor` class for data loading and processing.
- **`enhanced_predictor.py`**: Contains the `EnhancedPredictor` class defining the model architecture and training routines.
- **`enhanced_dashboard.py`**: Contains the `EnhancedDashboard` class for visualization during training.
- **`main.py`**: The main script that ties everything together. It loads the data, splits it into training and validation sets, trains the model, updates the dashboard, and saves the trained model.
- **`evaluate.py`**: Contains a function to load a saved model and evaluate its performance on a validation set with detailed plots.

## Requirements

Ensure you have the following dependencies installed:

- Python 3.6+
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [scikit-learn](https://scikit-learn.org/)
- [TensorFlow](https://www.tensorflow.org/)
- [Matplotlib](https://matplotlib.org/)

You can install the necessary packages via pip:

```bash
pip install pandas numpy scikit-learn tensorflow matplotlib
