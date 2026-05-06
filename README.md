
# 🧠 Alzheimer's Disease Detection using Deep Learning


Internship project — 2CS Computer Systems (SIQ) — ESI Algiers


---

## Overview

This project explores deep learning approaches for the automated
classification of Alzheimer's disease stages from T1-weighted MRI
images. It was developed as part of a supervised internship at CERIST.

Four CNN architectures are evaluated: **ResNet50**, **EfficientNetB2**,
**DenseNet169**, and **DenseNet201**, using a Weighted Probability-Based
Ensemble Method (WPBEM).

## Dataset

- Source: ADNI (Alzheimer's Disease Neuroimaging Initiative)
- Modality: T1-weighted 3T MRI (baseline scans)
- Classes: CN | EMCI | LMCI | AD
- Total slices: ~13,017 (after preprocessing)

## Results (Binary Classification)

| Task          | ResNet50 | DenseNet169 | EfficientNetB2 | DenseNet201 |
|---------------|----------|-------------|----------------|-------------|
| CN vs AD      | 94.8%    | 96.8%       | 97.1%          | 97.4%       |
| CN vs EMCI    | 93.9%    | 95.5%       | 95.6%          | 95.9%       |
| EMCI vs LMCI  | 84.3%    | 90.2%       | 91.3%          | 91.8%       |
| LMCI vs AD    | 98.9%    | 99.7%       | 99.8%          | 99.8%       |

## Tech Stack

Python · TensorFlow/Keras · SimpleITK · NiBabel · OpenCV · NumPy

## Project Structure

```
├── preprocessing/    # DICOM→NIfTI, skull strip, SSIM slice selection
├── models/           # ResNet50, EfficientNetB2, DenseNet169, DenseNet201
├── ensemble/         # WPBEM implementation
├── results/          # Confusion matrices, metrics
└── report/           # Internship report PDF
```


Data from ADNI (adni.loni.usc.edu) — not included in this repo.
  
