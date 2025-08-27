# README

## Project Overview
This repository contains data and scripts for training supervised classifiers (e.g., neural networks) on labeled acoustic datasets. The project is organized into three subsets:

- **Subset_A/**
- **Subset_B/**
- **Subset_C/**

Each subset has the following folder structure:

- **1_Original_Data/**  
  - `original_data_for_classification.xlsx`: Main dataset containing labels and extracted features required for building a supervised classifier.  
  - `Labeled_Data_With_Features.xlsx`: Source file used to generate `original_data_for_classification.xlsx`. This file should not be modified.  

- **2_Clean_Data/**  
  - `Labeled_Data_to_Review.xlsx`: File used to manually review and filter the dataset.  
  - `cleaned_data_for_classification.xlsx`: Cleaned version of the dataset. This is the dataset to be used for training the second set of models.  

Additionally, the repository includes a Jupyter notebook that was used to create both `original_data_for_classification.xlsx` and `cleaned_data_for_classification.xlsx` from the source files (`Labeled_Data_With_Features.xlsx` and `Labeled_Data_to_Review.xlsx`).

---

## Current Status
- Datasets have been organized into **original** and **cleaned** versions for each subset.  
- The project is ready for the model training phase.  

---

## Next Steps
For each subset (**A, B, C**):  
1. Train a model using **original data** (`original_data_for_classification.xlsx`).  
2. Train a model using **cleaned data** (`cleaned_data_for_classification.xlsx`).  
3. Use **K-fold cross-validation** during training to ensure robustness and reproducibility.  
4. Report the following metrics for each model:  
   - **F1 Score**  
   - **Accuracy**  
   - **Final Confusion Matrix**  

---

## Model Comparison
To evaluate the effect of data cleaning:  

- **Direct Metric Comparison:** Compare the mean F1 score and accuracy across folds between the original-data model and the cleaned-data model.  
- **Statistical Testing:** Perform a paired test (e.g., Wilcoxon signed-rank test or paired t-test) on F1 scores across folds to determine if the improvement is statistically significant.  
- **Confusion Matrix Analysis:** Compare confusion matrices to identify whether cleaning reduced specific types of misclassifications (e.g., noise mislabels).  
- **Visual Summary:** Plot side-by-side bar charts or boxplots of F1 scores and accuracies for original vs. cleaned models to provide a clear visual comparison.  

---

## Expected Outcome
This process will reveal whether dataset cleaning improves classification performance and whether the trade-off between data size and label quality is beneficial for the supervised task.  
