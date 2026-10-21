# EEG Motor Imagery Classification using IFNet

## Overview

This project implements a deep learning approach for classifying EEG motor imagery signals using an IFNet-based architecture.

The objective is to classify imagined motor activities from EEG signals without requiring physical movement.

## Motor Imagery Classes

The model performs classification for:

- Left Hand
- Right Hand
- Both Feet
- Tongue

## Methodology

The overall pipeline includes:

1. EEG data loading
2. EEG signal preprocessing
3. Signal filtering
4. Epoch generation
5. Data augmentation
6. Deep feature extraction
7. IFNet-based classification
8. Model training
9. Performance evaluation

## Dataset

This project uses the BCI Competition IV Dataset 2a.

The original dataset is not included in this repository due to dataset size and licensing considerations.

## Technologies

- Python
- PyTorch
- MNE
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project

The complete implementation is available in:

`MotorImagery.ipynb`

The notebook contains the preprocessing pipeline, model implementation, training procedure, and evaluation.

## Results

| Model | Accuracy |
|---|---:|
| Baseline | TBD |
| Proposed IFNet | TBD |

Results will be updated with the final experimental values.

## Kaggle

The project was developed and executed using Kaggle GPU infrastructure.

Kaggle Notebook:

`https://www.kaggle.com/code/shafishaik01/motorimagery/`

## How to Run

Clone the repository:

```bash
git clone https://github.com/Shaik-Shafi-01/IFNet-EEG-Motor-Imagery.git
