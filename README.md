# Brain Tumour Classification from MRI

## Overview
A deep learning project that classifies brain MRI images into four categories using MobileNetV2 transfer learning.

## Classes
- Glioma
- Meningioma
- Pituitary tumour
- No tumour

## Dataset
Brain Tumor MRI Dataset from Kaggle, containing approximately 7,200 images across training and testing folders.

Dataset: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

## Technologies
- Python
- TensorFlow / Keras
- MobileNetV2
- NumPy and Pandas
- Matplotlib and Seaborn
- Scikit-learn

## Methodology
1. Loaded and inspected the MRI dataset.
2. Resized images and prepared training, validation and testing datasets.
3. Trained a MobileNetV2 transfer-learning classifier.
4. Evaluated precision, recall, F1-score and the confusion matrix.
5. Compared baseline training, fine-tuning and data augmentation.
6. Investigated possible dataset bias using image dimensions and intensity statistics.

## Results

| Experiment | Test accuracy |
|---|---:|
| Original MobileNetV2 | 85.62% |
| Fine-tuned MobileNetV2 | 85.50% |
| Data augmentation experiment | 77.31% |
| Extended training | 86.44% |
| Metadata-only classifier | 63.19% |

The extended MobileNetV2 model achieved the highest observed test accuracy of 86.44%. Glioma remained the most challenging class, with 70% recall.

## Limitations
Image dimensions and intensity statistics alone achieved 63.19% accuracy, indicating that low-level image properties correlate with the class labels. This raises a potential dataset-bias concern but does not prove source-specific bias. Source-labelled or external-source evaluation is needed for stronger conclusions.

This project is for educational research and is not a clinically validated diagnostic system.
