# Performing Brain Tumor classification and Segmentation

## Brief Description

This project was designed by Swetaswa Basak and Paras PAtil, as our end year Masters degree in Software Engineering. The study segments and classifies MRI scans of brain tumours. The lack of use of EfficientNetB7, one of the top commonly used pre-trained transfer learning models, in the categorization of brain tumours served as the impetus for this effort. Therefore, we made the decision to compare it to the most recent, widely used, and best transfer learning model, VGG16. In this research, the accuracy, complexity, and training and prediction times of VGG16 and EfficientNetB7 are compared. Then put the Best model into practise in a web application.

###### _Keywords_
> `EfficientNetB7`, `VGG16`, `classification`,  `segmentation`, `transfer learning`, `pre-trained model`


**AUTHORS**

1. Swetaswa Basak, Vellore Institute of Technology, India
2. Paras Patil, Vellore Institute of Technology, India
3. Praneeth Prakash Namakar, Vellore Institute of Technology, India

## Overview

| **Table of Content**              | 
| --------------------------------- | 
| _Specifications and requirements_ | 
| _Content of project with results_ | 
| _Acknowledgements_                | 
| _Web Application_                 | 

## Specifications and requirements

Machine Specifications

| **Table of Content**   |   **Description**                                   |
| ---------------------- |  -------------------------------------------------- |
| `Operating system`     | Windows 10 & Windows 11 64-bit operating system     |
| `RAM`                  | 8GB & 16GB                                          |
| `Graphics`             | Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz   1.80 GHz |
| `Editors`              | Jupyter Notebbok, Spyder, Google Colab              |

Requirements

1. Python
2. Tensorflow
3. Keras
4. matplotlib
5. Streamlit

## Content of project with results

**1. Data Collection & Pre-Processing**

The data was downloaded from kaggle, Read the [README file](DataSet/README.md) to get the link for the dataset.

_A Glimpse of the data_

![DataSet](/README-images/DataSet.png)

_Pre-Processing of the data_

The images where transformed in the following manner

| **Transformation**               |   **OutPut**                                     |
| -------------------------------- |  ----------------------------------------------- |
| Original Image                   | ![Transformation](/README-images/original.png)   |
| horizontal flipping              | ![Transformation](/README-images/horizontal.png) |
| vertical flipping                | ![Transformation](/README-images/vertical.png)   |
| zooming at 0.2                   | ![Transformation](/README-images/zoom.png)       |
| rotation at 20 degrees           | ![Transformation](/README-images/rotation.png)   |
| featurewise_std_normalization    | ![Transformation](/README-images/featurewise.png)|
| shear-range of 0.2               | ![Transformation](/README-images/shear.png)      |
| brightening at the range 0.2-1.5 | ![Transformation](/README-images/brightness.png) |
| width shift range of 0.1         | ![Transformation](/README-images/width.png)      |
| height shift range of 0.1        | ![Transformation](/README-images/height.png)     |


**2. Model Development and Fine-tuning**

The following parameters namely: Batch size, Epochs, Dropout and Optimizer, of the model where fined, and the visualisation of the results are below

The following values and parameters where chosen:

- **_Optimizers_** - We will use only 5 optimizers to see which one works best, namely; `1. SGD,2. RMSprop,3. Adam,4. Adagrad,5. Adadelta.` the best optimizer will be used in the New model

- **_Number of epochs_** - We will also use only 4 epochs to choose the best performer namely; `1, 2, 5, 10.`

- **_Batch size_** - we will also use these batch sizes to choose the optimum batch size, namely; `8, 16.`

- **_Dropout_** - we will optimise the dropout of the model, values `0.5, 0.6, 0.7, 0.8, 0.9`

#### EfficientNetB7 - Batch size and Epochs

![FineTuning](/README-images/efn_bNe.png)       


#### VGG16 - Batch size and Epochs

![FineTuning](/README-images/vgg_bNe.png)


#### EfficientNetB7 - Dropout

![FineTuning](/README-images/efn_drop.png)


#### VGG16 - Dropout

![FineTuning](/README-images/vgg_drop.png)


#### EfficientNetB7 - Optimizer

![FineTuning](/README-images/efn_opt.png)


#### VGG16 - Optimizer

![FineTuning](/README-images/Screenshot_20211213-111155_Chrome.jpg)



**3. Final Model Implementation and Results**

This is the structure of the EfficientNetB7 model we implemented with optimum parameters, similarly with the VGG16 model.

![Model](/README-images/ModelEFN.png)

**4. Conclusions**

Our aim of our project was to compare VGG16 and EfficientNetB7, in terms of accuracy, complexity, and training time & prediction time(how long it takes to predict), 

And our study shows that EfficientNetB7 takes longer to predict than VGG16, and also its training Time takes longer, and the best model in terms of accuracy is EfficientNetB7 with 98.19% over VGG16 which is 92.30%, therefore for our web app we chose EfficientNetb7 even though it has a limitation of taking longer to predict other VGG16. 

## Acknowledgements

I appreciate and acknowledge the supervision of the project by Mrs Uma Maheswari, my TARP Project Lecturer at Vellore Institute of Technology, India in 2022.

Thank you.

