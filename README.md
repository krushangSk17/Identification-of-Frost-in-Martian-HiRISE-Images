[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/J0DgMjNz)

| **Field**        | **Information**   |
|-------------------|-------------------|
| **Name**          | Krushang Satani   |
| **USC-ID**        | 8931363113        |
| **Course**        | DSCI 552 DSML     |
| **Title**         | Final Project Summary  |


### 1. CNN + MLP Model
- **Architecture:** A custom sequential model with three convolutional layers, batch normalization, max pooling, a flatten layer, a dense layer, and an output layer. Regularization (L2) and dropout are used to prevent overfitting.
- **Methodology:** Trained for 21 epochs using TensorFlow datasets with augmented training data.
- **Performance Metrics:**
  - Best Validation Accuracy: 98.19%
  - Test Accuracy: 84.82%
  - Test Precision: 95.70%
  - Test Recall: 80.46%
  - F1 Score: 0.874
    
### 2. VGG16
- **Architecture:** Based on the VGG16 base model, with added layers including global average pooling, dense, batch normalization, dropout, and output layer. The base model layers are frozen.
- **Methodology:** Trained for 10 epochs with early stopping and model checkpoint callbacks. Used TensorFlow datasets with augmented training data.
- **Performance Metrics:**
  - Test Accuracy: 91.69%
  - Test Precision: 96.05%
  - Test Recall: 91.06%
  - F1 Score: 0.935

### 3. EfficientNetB0
- **Architecture:** Utilizes EfficientNetB0 as the base model, with added global average pooling, dense, batch normalization, dropout, and output layers. The base model layers are frozen.
- **Methodology:** Trained for 10 epochs with early stopping and model checkpoint callbacks on augmented TensorFlow datasets.
- **Performance Metrics:**
  - Test Accuracy: 65.55%
  - Test Precision: 65.55%
  - Test Recall: 100%
  - F1 Score: 0.792

### 4. ResNet50
- **Architecture:** Builds upon the ResNet50 base model with additional global average pooling, dense, batch normalization, dropout, and output layers. The base model layers are frozen.
- **Methodology:** Compiled with binary cross-entropy loss and metrics including accuracy, precision, and recall. Specific training methodology details are not provided.
- **Performance Metrics:**
  - Test Accuracy: 66.80%
  - Test Precision: 96.50%
  - Test Recall: 51.21%
  - F1 Score: 0.669



### Summary and Analysis
- The **CNN + MLP Model** and **VGG16** show higher test accuracies and F1 scores compared to **EfficientNetB0** and **ResNet50**. This could be due to the differences in architecture complexity and training methodologies.
- **EfficientNetB0** shows a perfect recall but relatively lower precision, indicating a tendency towards false positives.
- **ResNet50** has a high precision but lower recall, suggesting it is more conservative in predicting positive classes, leading to more false negatives.
- **VGG16** demonstrates a balanced performance with high precision and recall, resulting in the highest F1 score among the four.
- The choice of model depends on the specific application requirements, such as whether precision is more critical than recall or vice versa. For balanced overall performance, **VGG16** appears to be the most effective in this comparison.
