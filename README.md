# OCT Retinal Image Classification

A deep learning pipeline for classifying retinal Optical Coherence Tomography (OCT) 
scans into four diagnostic categories: **Normal, CNV, DME, and Drusen** — built and 
benchmarked across multiple model architectures to identify the optimal approach for 
clinical deployment.

## Overview

This project uses the OCT-MNIST dataset (MedMNIST v2) to design, train, and compare 
several classification approaches for automated retinal disease screening. Rather 
than relying on a single model, the pipeline benchmarks convolutional, ensemble, and 
sequential architectures against each other to surface the most clinically viable 
option.

## Models Implemented

- **CNN** (Convolutional Neural Network) — spatial feature extraction from raw images
- **MLP** (Multi-Layer Perceptron) — baseline dense network comparison
- **RNN** (Recurrent Neural Network) — sequential feature interpretation
- **SVC Bagging Ensemble** — bootstrap-aggregated support vector classifiers
- **Soft-Voting Ensemble** — probability-weighted combination of multiple classifiers

## Feature Engineering & Preprocessing

- Sobel edge detection for structural feature extraction
- Statistical feature extraction from image data
- PCA (Principal Component Analysis) for dimensionality reduction
- Min-max scaling for normalized model input

## Evaluation

All models were evaluated and compared on:
- Accuracy
- Precision
- Recall
- ROC-AUC

This multi-metric approach ensures the selected model isn't just accurate overall, 
but reliable across false-positive/false-negative tradeoffs — critical for a 
clinical screening tool.

## Tech Stack

`Python` · `scikit-learn` · `TensorFlow/Keras` · `NumPy` · `pandas` · `matplotlib`

## Dataset

[MedMNIST v2](https://medmnist.com/) — OCT-MNIST subset

## Motivation

Retinal OCT screening is a critical but resource-intensive diagnostic process. This 
project explores whether lightweight, benchmarked ML models can support faster, more 
accessible diagnostic triage — surfacing which architecture offers the best 
performance-to-complexity tradeoff for real-world clinical use.
