# BirdSpeciesIdentifier

## Overview
This project leverages machine learning techniques, specifically metric learning using Convolutional Neural Networks (CNN) with ArcFace, to develop a bird species classifier. The goal is to achieve high accuracy, contributing to ecological studies, biodiversity monitoring, and conservation efforts.

## Dataset
- **Dataset Used**: [BIRDS 525 SPECIES-IMAGE CLASSIFICATION](https://www.kaggle.com/datasets/gpiosenka/100-bird-species/discussion/389672)
- **Images**: 224x224x3 JPG format
- **Classes**: 525 bird species (reduced to 100 for this project)
- **Class Imbalance**: Varying number of images per species (min. 130, max. 263)
- **Gender Imbalance**: ~80% male, ~20% female

## Data Preprocessing
- **Normalisation**: Pixel values scaled from 0-255 to 0-1
- **Resizing**: Images resized to 96x96x3
- **Class Reduction**: Dataset reduced to first 100 classes.

## Model Architecture
- **Network Topology**: VGG-like CNN with layers [16, 32, 64, 64]
- **Embedding**: 128-dimensional
- **Loss Function**: ArcFace (Additive Angular Margin Loss)
- **Optimizer**: Adam
- **Learning Rate**: 0.001
- **Batch Size**: 246

## Training
- **Epochs**: 21 (optimal performance at epoch 18)
- **Training Time**: 28.9 ms per step
- **Inference Time**: 1.32 seconds
- **Hardware**: Hosted GPU

## Results
- **Validation Loss**: 1.3314
- **Validation Accuracy**: 0.9860
- **Convergence**: Achieved at epoch 18

## Limitations
- **Computational Resources**: Limited resources impacted the ability to scale and manage class centers efficiently.

