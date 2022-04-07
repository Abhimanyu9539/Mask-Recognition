# Real Time Mask Recognition 

During the times of Social Distancing and Covid Regularization, wearing masks has been crucial.
This POC works on the concept of distingushing the individuals based on if they are wearing masks or not.

# Dataset 
https://www.kaggle.com/datasets/techzizou/labeled-mask-dataset-yolo-darknet

# Darknet 
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation
Using YOLOv4 pre-trained weights and training them for identifying mask wearers from those are not wearing the masks.

# Files Required

## obj.data file
Classes = Number of classes which to be recognized
Train text file path
Test text file path
Backup folder path

## obj.names file
Names of classes ( With_mask, Without_mask)

## Preprocess file
python file to generate the file path of train and test files


