# Machine Learning-Based Classification of Eucalyptus Species: A Comparative Evaluation

## Overview
This project focuses on utilizing machine learning techniques to predict the species of Eucalyptus plants. The primary objective is to develop and compare various machine learning models to determine which one best predicts Eucalyptus species based on selected features.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Description](#dataset-description)
- [Data Exploration and Pre-processing](#data-exploration-and-pre-processing)
- [Modeling](#modeling)
- [Results and Discussion](#results-and-discussion)
- [Conclusions](#conclusions)
- [References](#references)
- [Reproducing Results](#reproducing-results)

## Introduction
This project utilizes machine learning techniques to predict the species of Eucalyptus plants, which is crucial for research, conservation, and a deeper understanding of each plant. We implemented several methods, including Linear Discriminant Analysis, K-Nearest Neighbors, Random Forest, and Support Vector Machine.

## Dataset Description
We selected the 'Eucalyptus' dataset from the OpenML website. The dataset includes numerical and categorical variables. It encompasses several species of Eucalyptus, featuring various attributes that can potentially distinguish one species from another.

### Original Dataset Characteristics:
- **Sample Size:** 736
- **Features:** 20
- **Missing Values:** 448 missing values across 95 samples
- **Target:** Species
- **Number of Species:** 25

## Data Exploration and Pre-processing
We addressed issues with data representation, missing values, outliers, and converted categorical variables for model compatibility. Additionally, we handled class imbalances to improve model performance.

### Steps:
1. **Feature Selection:** Simplified the model by eliminating redundant and irrelevant features.
2. **Target Representation Threshold:** Focused on target classes with more than 10 samples.
3. **Data Cleaning:** Addressed missing values and outliers, and scaled numerical data.
4. **Final Pre-processed Dataset Characteristics:**
   - **Final Sample Size:** 663
   - **Features:** 16
   - **Target:** Species
   - **Number of Species:** 17

## Modeling
We implemented and compared various machine learning models focusing and classses with more than 10 samples and we tried as well grouping classes with fewer than 10 samples into a single category. 
1. **Linear Discriminant Analysis (LDA):** Achieved an F1 macro score of 0.329.
2. **K-Nearest Neighbors (K-NN):** Best hyperparameters were 3 neighbors, Manhattan distance, and distance weights, achieving an F1 macro score of 0.284.
3. **Random Forest:** The best implementation achieved an F1 macro score of 0.520 with optimized hyperparameters.
4. **Support Vector Machine (SVM):** Best hyperparameters achieved an F1 macro score of 0.367.

## Results and Discussion
The Random Forest model with optimized hyperparameters performed the best among all the models. Grouping classes with fewer than 10 samples into a single category did not lead to overall performance improvements.

## Conclusions
The Random Forest model proved to be the most effective for our dataset, handling class imbalances and achieving the highest F1 macro score. Despite the dataset's limitations, the model was configured to optimally handle potential difficulties, ensuring high-quality performance. Future improvements could include collecting more data and exploring different clustering strategies for similar species.

## References
- Bulloch, B. (2014). Eucalyptus Soil Conservation OpenML. WEKA Dataset Collection.
  https://www.openml.org/search?type=data&status=active&id=188&sort=runs

## Reproducing Results
To reproduce the results from the provided Python notebook `final_project_eucalyptus.ipynb`, follow these steps using Google Colab:
1. Upload the notebook and the dataset file `dataset_eucalyptus_neta.txt` to your Colab environment.
2. Ensure the dataset file is in the same directory as the notebook or adjust the file path in the notebook accordingly.
3. Install the required Python package `dython` by executing the command `!pip install dython` in a Colab cell.
4. Once the package is installed, execute all cells in the notebook by selecting `Runtime -> Run All`.

Following these steps will allow you to execute the notebook and reproduce the results discussed in the project report.


---

This project is part of the Bachelor’s Degree in Data Science and Engineering by **Maria Sans Bosch** and **Raquel Jolis Carné**, completed in May 2024.

