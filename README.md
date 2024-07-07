# Melanoma Detection Assignment

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## General Information
#### Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
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
 

NOTE: You don't have to use any pre-trained model using Transfer learning. All the model building process should be based on a custom model.

## Technologies Used
- pandas
- matplotlib
- tensorflow
- keras
- Augmentor
- google colab
- google drive

## Conclusions
- We started with a simple CNN model with following configuration:
    - Rescaling Layer - for scaling pixel values in 0-1 range
    - Convolutional Layer 1 - 32 filters with 3x3 kernel size and ReLU Activation
    - Max Pooling Layer 1 - 3x3 pool size
    - Convolutional Layer 2 - 64 filters with 3x3 kernel size and ReLU Activation
    - Max Pooling Layer 2 - 3x3 pool size
    - Convolutional Layer 3 - 128 filters with 3x3 kernel size and ReLU Activation
    - Max Pooling Layer 3 - 3x3 pool size
    - Flatten Layer
    - Dense Layer 1 - 512 units and ReLU Activation
    - Output Layer - Dense layer with softmax activation for the 9 output classes
- This provided an overfitting model with high training accuracy and low validation accuracy
- We built a second model by adding augmentation, dropouts, L2 regularization which removed the overfitting. But accuracy rate was still 52-56%
- We used augmentor to remove the class imbalance by creating more samples in each classes. 
- We built a third model with more samples removing class imbalance, introducing batch normalization and increasing the number of epochs. This increased the accuracy but more number of epochs seems to have introduced more overfitting.


## Contact
Created by [@prasune] - feel free to contact me!