# Medical Image Segemntation Deep Learning Project

To segment the polyps from colonoscopy images

## Overview
Machine learning and deep learning technologies are increasing at a fast pace with respect to the domain of healthcare and medical sciences. These technologies sometimes even outperform medical doctors by producing results that might not be easily notable to the human eye. Polyp recognition and segmentation is one such technology that helps doctors identify polyps from colonoscopic images.

## Data
The CVC-Clinic database consists of frames extracted from colonoscopy videos. The dataset contains several examples of polyp frames & corresponding ground truth forthem. The Ground Truth image consists of a mask corresponding to the region covered by the polyp in the image. The data is available in both .png and .tiff formats

_Data is not included in this repository._

## Approach
1. Data Understanding: Understanding the essence of the dataset
2. Understanding evaluation metrics: Understanding the metrics that are going to be used for evaluating the predictions
3. Unet Architecture : Understanding Unet architecture and why is it preferred widely in building deep learning models with respect to medical sciences.
4. Unet ++ : Understanding Unet++ and how is it different from Unet
5. Environment Setup:

Setting up a working environment for the project
6. Data Augmentation: Creating new data by making modifications on the existing data
7. Model building: Building Unet ++ model using pytorch
8. Model Training Training the model. ( A GPU might be required since model training takes a really long time in CPUs)
9. Model Prediction

Modular code overview

Once you unzip the modular_code.zip file you can find the following folders within it.
1. input
2. src
3. output
4. lib
5. requirements.txt
1. The input folder contains all the data that we have for analysis. In our case, it will contain two folders namely.

a. PNG b. TIF `      The PNG folder contains the images used for training the model in .png format while the TIF folder contains the same set of images in .tiff format
2. The src folder is the heart of the project. This folder contains all the modularized code for all the above steps in a modularized manner. It further contains the following. a. ML_pipeline b. engine.py c. config.yaml

The ML_pipeline is a folder that contains all the functions put into different python files which are appropriately named. These python functions are then called inside the engine.py file. The config.yaml file contains various project constants that can be altered according to users’ needs.

3. The output folder contains the model that we trained for this data saved as a reusable file. It also contains the predicted images
4. The lib folder is a reference folder. It contains the original ipython notebook that was shown in the videos
5. Finally, the requirements.txt consists of all the packages and libraries used in the project.

## Tech stack
Language used: Python Deep learning library used: Pytorch Computer vision library used: OpenCV Other python libraries: Scikit-learn, pandas, numpy, albumentations etc.

## How to run
```bash
pip install -r Modular_code_updated/requirements.txt
python Modular_code_updated/train.py
```
Notebooks: [`UNet.ipynb`](Modular_code_updated/UNet.ipynb)

## Project structure
```
.gitignore
Modular_code_updated/
  README.md
  UNet.ipynb
  config.yaml
  predict.py
  requirements.txt
  source/
    dataset.py
    network.py
    utils.py
  train.py
README.md
```

## Credits
Based on a ProjectPro guided project.
