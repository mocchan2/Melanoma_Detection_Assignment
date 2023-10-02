# Project Name
> Melanoma Detection Assignment.


## Table of Contents
* Project Pipeline
1. Data Reading/Data Understanding → Defining the path for train and test images 
2. Dataset Creation→ Create train & validation dataset from the train directory with a batch size of 32. 
3. Dataset visualisation → Create a code to visualize one instance of all the nine classes present in the dataset 
4. Model Building & training : 
-- Create a CNN model, which can accurately detect 9 classes present in the dataset. 
-- Choose an appropriate optimiser and loss function for model training
-- Train the model for ~20 epochs
-- Write the findings after the model fit. Check if there is any evidence of model overfit or underfit.
5. Chose an appropriate data augmentation strategy to resolve underfitting/overfitting 
6. Model Building & training on the augmented data :
-- Create a CNN model, which can accurately detect 9 classes present in the dataset. 
-- Choose an appropriate optimiser and loss function for model training
-- Train the model for ~20 epochs
-- Write the findings after the model fit, see if the earlier issue is resolved or not.
7. Class distribution: Examine the current class distribution in the training dataset 
-- Which class has the least number of samples?
-- Which classes dominate the data in terms of the proportionate number of samples?
8. Handling class imbalances: Rectify class imbalances present in the training dataset with Augmentor library.
9. Model Building & training on the rectified class imbalance data :
-- Create a CNN model, which can accurately detect 9 classes present in the dataset. 
-- Choose an appropriate optimiser and loss function for model training
-- Train the model for ~30 epochs
-- Write the findings after the model fit, see if the issues are resolved or not.
 
## General Information
- What is the background of your project?
* Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

- What is the business probem that your project is trying to solve?
* To build a CNN based model which can accurately detect melanoma. To build a multiclass classification model using a custom convolutional neural network in TensorFlow.

- What is the dataset that is being used?
* The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
-- Actinic Keratosos and Seborrheic keratosis have the least number of samples.
-- Pigmented benign keratosis dominates the data in terms of the proportionate number of samples with more than 100 counts in training data. 
-- The class rebalance helped in reducing overfititng of the data and thus the loass is beng reduced But it reduced the Acurracy very low.
-- Initially we tried without the ImageDataGenerator which created data to over fit at high ratio.
-- Then we introduced dropout and ImageDataGenerator which reduced the over fit.
-- At last we tried Batch Normalization and Augumentation which really helped in carry forward.

