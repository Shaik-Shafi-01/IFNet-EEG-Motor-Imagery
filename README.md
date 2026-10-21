# EEG Motor Imagery Classification using IFNet

Deep learning-based EEG motor imagery classification using an IFNetV2 architecture with Euclidean Alignment, filter-bank preprocessing, data augmentation, 5-fold ensemble learning, and multi-window test-time augmentation.

## Overview

Motor imagery (MI) is the process of imagining a physical movement without actually performing it. EEG signals recorded during motor imagery contain patterns that can be used by Brain-Computer Interface (BCI) systems to identify the intended movement.

This project implements an IFNet-based deep learning pipeline for four-class motor imagery classification using the BCI Competition IV Dataset 2a.

The project focuses on improving cross-session EEG classification by combining:

- Euclidean Alignment
- Two-band filter-bank preprocessing
- Subject-adaptive preprocessing
- Random temporal cropping
- CutMix augmentation
- Random Erasing
- Repeated Trial Augmentation
- IFNetV2 deep learning architecture
- 5-fold ensemble learning
- Multi-window Test-Time Augmentation (TTA)

---

## Motor Imagery Classes

The model performs four-class classification:

| Class | Motor Imagery |
|-------|---------------|
| 0 | Left Hand |
| 1 | Right Hand |
| 2 | Both Feet |
| 3 | Tongue |

---

## Dataset

This project uses the **BCI Competition IV Dataset 2a**.

The dataset contains EEG recordings from 9 subjects performing four-class motor imagery tasks.

### Dataset characteristics

- Subjects: 9
- EEG channels: 22
- Sampling frequency: 250 Hz
- Motor imagery classes: 4
- Sessions: Training and evaluation sessions
- Evaluation: Cross-session classification

The dataset is **not included in this repository** because of its size and distribution considerations.

---

# Methodology

The complete pipeline implemented in the notebook is:

```text
BCI Competition IV-2a
        │
        ▼
Training / Evaluation Sessions
        │
        ▼
Subject-Specific Preprocessing
        │
        ├── Euclidean Alignment
        │
        ▼
Two-Band Filter Bank
        │
        ├── 4–16 Hz
        └── 16–40 Hz
        │
        ▼
Normalization
        │
        ▼
Data Augmentation
        │
        ├── Random Crop
        ├── CutMix
        ├── Random Erasing
        └── Repeated Trial Augmentation
        │
        ▼
750-Sample EEG Input
        │
        ▼
IFNetV2
        │
        ▼
5-Fold Training
        │
        ▼
Multi-Window TTA
        │
        ▼
5-Fold Ensemble
        │
        ▼
Cross-Session Evaluation
