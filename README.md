# VGG16-Functional-APIs

This code is an example of building a deep learning model for predicting both age and gender from facial images in a single neural network. It uses the VGG16 architecture as a feature extractor and employs a Functional API for creating a multi-output model.

## About Dataset

- **UTKFace dataset** is a large-scale face dataset with a wide age span (ranging from 0 to 116 years old).
- The dataset consists of over 20,000 face images with annotations of age, gender, and ethnicity.
- The images cover a significant variation in pose, facial expression, illumination, occlusion, resolution, etc.
- Consists of 23k+ face images in the wild, with only a single face in each image.
- Images are labeled by age, gender, and ethnicity.
  - Age: An integer from 0 to 116, indicating the age.
  - Gender: 0 (male) or 1 (female).
  - Race: An integer from 0 to 4, representing White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern).
  - Date & Time: In the format of yyyymmddHHMMSSFFF, showing the date and time an image was collected for UTKFace.

[UTKFace Dataset Link](https://www.kaggle.com/datasets/jangedoo/utkface-new)

## Model Building Process

1. Froze the pre-trained layers to prevent them from being updated during training.
2. Defined additional layers for age and gender prediction on top of VGG16.
3. Created a multi-output model with separate outputs for age and gender and compiled it with appropriate metrics, optimizers, and loss functions.

## Key Achievements and Observations

1. **Age Prediction:**
   - Mean Absolute Error (MAE) on the training set gradually decreases from approximately 9.73 to 8.14 as training progresses over 10 epochs.
   - MAE on the validation set follows a similar decreasing trend, reaching around 8.67.

2. **Gender Prediction:**
   - Accuracy on gender prediction for the training set starts at 77.78% and increases to 83.13% after 10 epochs.
   - On the validation set, the accuracy improves from 83.36% to 87.06% during training.

3. **Overall Loss:**
   - The total loss decreases over epochs, indicating the model's learning progress.

4. These results suggest that the model is learning to predict both age and gender effectively, with decreasing MAE for age prediction and increasing accuracy for gender prediction over the training process.

<br><br>
<ins> **NOTE:** </ins> Race feature has not been extracted due to poor annotations in the dataset.
<br><br>
[**BLOG LINK**](https://rajkulkarni.hashnode.dev/functional-api-transfer-learning)
