# README

## Project Overview

This repository contains data and scripts for training supervised classifiers (e.g., neural networks) on labeled acoustic datasets. The project is organized into three subsets:

- **Subset_A/**
- **Subset_B/**
- **Subset_C/**

Each subset has the following folder structure:

- **1_Original_Data/**  
  - `original_data_for_classification.csv`: Main dataset containing labels and extracted features required for building a supervised classifier.  
  - `Labeled_Data_With_Features.xlsx`: Source file used to generate `original_data_for_classification.csv`. This file should not be modified.  

- **2_Clean_Data/**  
  - `Labeled_Data_to_Review.xlsx`: File used to manually review and filter the dataset.  
  - `cleaned_data_for_classification.csv`: Cleaned version of the dataset. This is the dataset to be used for training the second set of models.  

The repository includes a Jupyter notebook that was used to create both `original_data_for_classification.csv` and `cleaned_data_for_classification.csv` from the source files (`Labeled_Data_With_Features.xlsx` and `Labeled_Data_to_Review.xlsx`).

The training and evaluation pipeline implemented is contained within `train_and_eval.ipynb`. SVM models are tuned individually for both versions of every subset. Metrics reported include:

   - **F1 Score**: Overall and per-fold.
   - **Accuracy**: Overall and per-fold.
   - **Final Confusion Matrix**
   - **Statistical Testing**: A Wilcoxon signed-rank test on F1 scores across folds is used to determine if the improvement is statistically significant.  
   - **Visual Summary**: Boxplots compare overall F1-Score and Accuracy performance across both versions of all subsets.
