# Alzheimer’s Disease Classification Using PET Images

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <!-- Optional: Add a license badge if applicable -->

## Overview
This project explores the use of deep learning, specifically Convolutional Neural Networks (CNNs), for classifying brain Positron Emission Tomography (PET) images. We utilize transfer learning with popular architectures—VGG16, InceptionV3, and ResNet50—to distinguish between three cognitive stages:
- Cognitively Normal (CN)
- Early Mild Cognitive Impairment (EMCI)
- Alzheimer’s Disease (AD)

The models are trained and evaluated using Amyloid PET images.
## Objective
The primary goal is to develop and evaluate a robust deep learning model capable of accurately classifying brain PET scans for the early detection of Alzheimer's Disease. Early detection is crucial for timely intervention, potentially slowing disease progression and improving patient outcomes.

## Data Source
- Dataset obtained from the Alzheimer’s Disease Neuroimaging Initiative (ADNI) repository.
- Images are split into training, validation, and test sets to ensure unbiased performance evaluation.

**Important:** Access to the ADNI dataset is restricted. Researchers must apply for access through the ADNI website. See the [How to Run](#how-to-run) section for more details.

## Methodology
1.  **Preprocessing:** Standard preprocessing steps were applied, including:
    *   Image resizing to meet model input requirements.
    *   Normalization of pixel values.
    *   Data augmentation techniques (e.g., rotation, flipping) to increase dataset robustness.
2.  **Model Selection:** Transfer learning was employed using CNNs pre-trained on the ImageNet dataset:
    *   VGG16
    *   Inception V3
    *   ResNet50
3.  **Training Strategy:**
    *   The pre-trained base models were frozen, and only the final classification layers were fine-tuned.
    *   Techniques like early stopping, learning rate scheduling, and dropout were used to mitigate overfitting and optimize training.

## Results
Performance varied across the models:
- **VGG16:** Demonstrated the strongest performance, achieving an accuracy exceeding 95% on the test set. It also proved relatively efficient in terms of computational resources.
- **Inception V3:** Also performed well, with accuracy slightly below VGG16 but still above 95%.
- **ResNet50:** Showed significantly lower performance, with accuracy around 40%, suggesting potential challenges in adapting this specific architecture to the nuances of the PET image data in this configuration.

**Conclusion:** Based on these results, VGG16 emerged as the most effective model for this specific task and dataset configuration, balancing high accuracy with reasonable computational demands.

## Future Work
Potential directions for future research include:
- Integrate additional data modalities (e.g., MRI, clinical data).
- Explore more advanced data augmentation strategies and hyperparameter tuning.
- Evaluate on larger, more diverse datasets.
- Investigate different model architectures or custom CNN designs.
- Implement explainability techniques (e.g., Grad-CAM) to understand model predictions better.

## How to Run

### Prerequisites
- Python 3.x
- Libraries: TensorFlow/Keras, NumPy, Matplotlib, Scikit-learn, etc. (Consider adding a `requirements.txt` file)

### Installation
1.  Clone the repository:
    ```bash
    git clone <https://github.com/Abdoul1996/Alzheimer_Classification> 
    cd Alzheimer_Classification
    ```
2.  Install required packages (assuming you create a requirements file):
    ```bash
    pip install -r requirements.txt
    ```

### Data Acquisition
**Crucially, the ADNI dataset used in this project is not publicly available and requires an application process.**
1.  Visit the ADNI Website.
2.  Follow their procedures to apply for data access.
3.  Once access is granted, download the relevant Amyloid PET image data.
4.  Organize the data into `train`, `validation`, and `test` directories within a main data folder (e.g., `./data/train`, `./data/validation`, `./data/test`). Ensure your scripts point to this structure.

## License
This project is licensed under the MIT License - see the `LICENSE.md` file for details. (You should create a file named `LICENSE.md` in the root directory containing the MIT license text).
