# Pneumonia Disease Detection Using Chest X-rays with Convolutional Neural Network (CNN)


![Python](https://img.shields.io/badge/Python-3.8+-green)
![Jupyter Notebook](https://img.shields.io/badge/Tools-Jupyter%20Notebook-orange)
![Scikit-learn](https://img.shields.io/badge/Library-Scikit--learn-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-lightblue)

## Project Overview

This project involves developing a deep-learning model to detect pneumonia from chest X-ray images using a Convolutional Neural Network (CNN). Pneumonia is a serious respiratory infection that requires prompt diagnosis and treatment. By leveraging the power of CNNs, this project aims to create an automated tool that assists in the early detection of pneumonia, thereby aiding healthcare professionals in making timely and accurate diagnoses.

## Objectives
-Develop a convolutional neural network (CNN) to classify chest X-ray images as either pneumonia-infected or healthy.

-Improve diagnostic accuracy and reduce the time required for diagnosis.


## Table of Contents

- [Introduction](#introduction)
- [Objective](#objective)
- [Dataset Description](#dataset-description)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modelling](#modelling)
- [K Means Clustering](#k-means-clustering)
- [Model Evaluation](#model-evaluation)
- [Reasult](#reasult)
- [Dependencies](#dependencies)
- [How to Run](#how-to-run)

## Introduction

Pneumonia is an inflammatory condition of the lung that primarily affects the air sacs and can be life-threatening if not diagnosed and treated promptly. Chest X-rays are a common diagnostic tool for detecting pneumonia. However, manual interpretation of X-rays requires expertise and can be time-consuming. This project leverages Convolutional Neural Networks (CNNs) to automate the detection of pneumonia from chest X-ray images, providing a reliable and efficient diagnostic tool

## Dataset Description

The dataset used in this project is sourced from the Kaggle Pneumonia Detection Dataset. It consists of 5,863 labelled X-ray images, divided into two categories: "Pneumonia" and "Normal".

Training Set: 4,200 images
Validation Set: 600 images
Test Set: 1,063 images
The dataset is well-suited for binary classification tasks and is pre-split into training, validation, and test sets

Acess data source :  https://www.cell.com/cell/fulltext/S0092-8674(18)30154-5

Dataset link: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

## Data Preprocessing

- Image Resizing: All images were resized to 224x224 pixels to ensure uniformity across the dataset.
  
- Normalization: Pixel values were normalized to the range [0, 1] to facilitate faster convergence during training.
  
- Data Augmentation: Techniques such as rotation, zooming, and flipping were applied to the training data to improve the model's generalization capability.


## Model Architecture

The model architecture is based on a deep Convolutional Neural Network (CNN), which is designed to automatically and adaptively learn spatial hierarchies of features from input images. The architecture includes:

- Convolutional Layers: For feature extraction.
  
- Pooling Layers: For dimensionality reduction.
  
- Fully Connected Layers: For classification.
  
- Dropout Layers: To prevent overfitting.


## Model Training

- Loss Function: Categorical cross-entropy was used as the loss function.
  
- Optimizer: The Adam optimizer was employed for training.
  
- Learning Rate Scheduling: A learning rate scheduler was used to reduce the learning rate dynamically as training progressed.
  
- Early Stopping: Implemented to halt training when the validation loss stopped improving, preventing overfitting.


 ## Model Evaluation:

- The model's performance was evaluated using metrics such as accuracy, precision, recall, and the F1-score.

- The confusion matrix was analyzed to assess the model's capability in distinguishing between pneumonia-infected and healthy images.

## Results

- Accuracy: The model achieved an accuracy of 96% on the test set.

- Precision: The precision for detecting pneumonia was 99%, reducing the likelihood of false positives.

- Recall: The recall was 94%, indicating the model's effectiveness in identifying true positive cases.

- F1-Score: The F1-score was 97%, reflecting a strong balance between precision and recall.

## Challenges and Solutions

- Model Interpretability: Implemented Grad-CAM (Gradient-weighted Class Activation Mapping) to visualize which areas of the X-ray image the model focused on, helping users understand the model’s decision-making process.
  
- Data Imbalance: Addressed the imbalance between pneumonia and normal cases by using data augmentation and a weighted loss function to improve model performance.

  






## How to Run

To run the project:
1. Clone this repository.
2. Install the required dependencies.
3. Open the Jupyter Notebook and execute the cells to train and evaluate the model.

```bash
git clone https://github.com/yasirsaleem502/Customer-Segmentation-with-K-Means-Clustering.git
cd customer-segmentation
pip install -r requirements.txt
