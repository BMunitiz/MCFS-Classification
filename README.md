# ME/CFS Metabolomics Classification Analysis

This repository contains a Jupyter notebook that performs machine learning classification of ME/CFS (Myalgic Encephalomyelitis/Chronic Fatigue Syndrome) patients from healthy controls using metabolomics data.

## Project Overview

This analysis uses metabolomic profiling data to identify metabolic signatures that distinguish ME/CFS patients from healthy individuals. The study employs multiple machine learning approaches to classify samples based on their metabolomic profiles.

## Dataset Description

The dataset includes:
- 52 samples (26 ME/CFS cases, 26 healthy controls)
- 1790 metabolomic compounds measured
- Sample metadata including health status labels

## Analysis Methods

### Data Preprocessing
1. **Data Loading**: Load metabolomics data and sample metadata from CSV files
2. **Feature Selection**: Select features with correlation > 0.3 with target variable
3. **Train/Test Split**: Stratified split to preserve class balance (80/20)
4. **Scaling**: Standard scaling for models requiring it

### Models Implemented
1. **Logistic Regression** (with feature selection and scaling)
2. **Random Forest** (with feature selection)
3. **Decision Tree** (with feature selection)
4. **Neural Network** (with feature selection and scaling)

## Key Results

- Selected 31 features with correlation > 0.3 for classification (not 18 as previously stated)
- Model performance on test set:
  - Neural Network: Accuracy 0.9091, AUC 0.9667
  - Logistic Regression: Accuracy 0.9091, AUC 0.967
  - Random Forest: Accuracy 0.733, AUC 0.933
  - Decision Tree: Accuracy 0.533, AUC 0.717

## Visualizations Included

The enhanced notebook includes several visualizations:
- Feature importance plots showing correlations with health status
- Confusion matrix comparisons for all models
- ROC curves for model discrimination ability
- Box plots showing distribution of key metabolites between cases and controls

## Usage

To run the analysis:
1. Ensure all required Python packages are installed (`pandas`, `numpy`, `scikit-learn`, `tensorflow`, `matplotlib`, `seaborn`)
2. Open `MCFS_analysis.ipynb` in Jupyter Notebook or compatible environment
3. Execute cells sequentially to reproduce the analysis

## Implications

This work demonstrates that specific metabolic signatures can be used to distinguish ME/CFS patients from healthy controls, which could have implications for:
- Diagnosis of ME/CFS
- Monitoring treatment response
- Understanding disease mechanisms