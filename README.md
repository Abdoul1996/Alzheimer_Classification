# Alzheimer_Classification

## Alzheimer’s Disease Classification Using PET Images

## Overview
This project leverages deep learning models—VGG16, InceptionV3, and ResNet50—to classify brain PET images into three categories:
- Cognitively Normal (CN)
- Early Mild Cognitive Impairment (EMCI)
- Alzheimer’s Disease (AD)

## Objective
The goal is to develop a reliable classification model for early-stage Alzheimer’s detection using Amyloid PET images, thereby supporting timely intervention and improving patient outcomes.

## Data Source
- Dataset obtained from the Alzheimer’s Disease Neuroimaging Initiative (ADNI) repository.
- Images are split into training, validation, and test sets to ensure unbiased performance evaluation.

## Methodology
- **Preprocessing:** Image resizing, normalization, and data augmentation.
- **Models:** Transfer learning from pre-trained CNNs (VGG16, Inception V3, ResNet50).
- **Training Strategy:** Fine-tuning classifier layers, using early stopping, learning rate scheduling, and dropout to prevent overfitting.

## Results
- **VGG16 & Inception V3:** Achieved high accuracy (>95%), with VGG16 slightly outperforming Inception V3.
- **ResNet50:** Underperformed (~40% accuracy), indicating that not all pre-trained architectures are equally effective for this task.
  
**Conclusion:** VGG16 emerged as the most accurate and computationally efficient model.

## Future Work
- Consider integrating additional data modalities (e.g., MRI, clinical data).
- Explore more advanced data augmentation strategies and hyperparameter tuning.
- Evaluate on larger, more diverse datasets.

## How to Run

**Note:** The dataset used in this project is subject to restricted access. If you are interested in running this code, please contact the authors for guidance on how to obtain the necessary permissions and access to the data.