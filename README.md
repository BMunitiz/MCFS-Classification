# ME/CFS Metabolomics Classification

This project implements machine learning and deep learning models for classifying Myalgic Encephalomyelitis/Chronic Fatigue Syndrome (ME/CFS) based on comprehensive metabolomics data.

## Overview

The notebook performs binary classification to distinguish between ME/CFS cases and healthy controls using metabolomic profiling data. It includes:

- Data preprocessing and exploratory analysis
- Multiple machine learning classifiers
- Deep learning models with TensorFlow/Keras
- Feature selection based on correlation analysis
- Model evaluation and performance comparison

## Dataset

The project uses two main data files:

1. **`data_matrix-table 1.csv`** - Contains metabolomics measurements for 1,790 compounds across 52 samples
2. **`sample_metadata-Table 1.csv`** - Contains sample metadata including health status labels

### Data Characteristics
- **Samples**: 52 total (mixed cases and controls)
- **Features**: 1,790 metabolic compounds
- **Target**: Binary classification (case vs control)

## Models Implemented

### Traditional Machine Learning
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Classifier
- Random Forest Classifier
- Naive Bayes
- Gradient Boosting Classifier

### Deep Learning
- Multi-Layer Perceptron (MLP) with scikit-learn
- Custom Neural Network with TensorFlow/Keras
  - Architecture: Input → Dense(32) → Dense(16) → Dense(8) → Output
  - Activation: ReLU for hidden layers, Sigmoid for output
  - Optimizer: Adam
  - Loss: Binary Crossentropy

## Key Features

### Data Preprocessing
- Data transposition for proper sample-feature orientation
- Handling of special characters and decimal formats in CSV files
- One-hot encoding of categorical labels
- Train-test split (80-20)
- Standard scaling for normalization

### Feature Selection
- Correlation analysis to identify metabolites most relevant to ME/CFS status
- Selection of top 31 features based on correlation coefficients (>0.3)

### Model Evaluation
- Accuracy scores
- Classification reports (precision, recall, F1-score)
- Confusion matrices
- Training history visualization for neural networks

## Results

The models show varying performance levels, with the custom TensorFlow model achieving high training accuracy (approaching 100%) after 300 epochs, though this may indicate potential overfitting given the small dataset size.

## Usage

1. Ensure required dependencies are installed:
   ```bash
   pip install pandas numpy tensorflow scikit-learn matplotlib seaborn
   ```

2. Place the data files in the working directory:
   - `data_matrix-table 1.csv`
   - `sample_metadata-Table 1.csv`

3. Run the Jupyter notebook sequentially to:
   - Load and preprocess data
   - Train various classification models
   - Evaluate model performance
   - Perform feature selection
   - Train deep learning models

## Dependencies

- Python 3.x
- pandas
- numpy
- tensorflow/keras
- scikit-learn
- matplotlib
- seaborn


This project demonstrates a comprehensive approach to metabolomics-based classification of ME/CFS, combining traditional machine learning with modern deep learning techniques.
