# VGG16-Functional-APIs

This code is an example of building a deep learning model for predicting both age and gender from facial images in a single neural network. It uses the VGG16 architecture as a feature extractor and employs a Functional API for creating a multi-output model.

## About Dataset
1. UTKFace dataset is a large-scale face dataset with long age span (range from 0 to 116 years old).
2. The dataset consists of over 20,000 face images with annotations of age, gender, and ethnicity.
3. The images cover large variation in pose, facial expression, illumination, occlusion, resolution, etc.
4. Consists of 23k+ face images in the wild (only single face in one image).
5. Images are labelled by age, gender, and ethnicity.
6. age - is an integer from 0 to 116, indicating the age
   gender is either 0 (male) or 1 (female)
   race is an integer from 0 to 4, denoting White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern).
   date&time is in the format of yyyymmddHHMMSSFFF, showing the date and time an image was collected to UTKFace
7. [UTKFace Dataset Link -](https://www.kaggle.com/datasets/jangedoo/utkface-new)

## Model Building process
1. Froze the pre-trained layers to prevent them from being updated during training.
2. Defined additional layers for age and gender prediction on top of VGG16.
3. Created a multi-output model with separate outputs for age and gender and compiled it appropriate metrics, optimizers and loss functions.

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

**NOTE** - Race feature has not been extracted due to poor annotations in the dataset. 

