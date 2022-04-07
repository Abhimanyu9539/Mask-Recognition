# Real Time Mask Recognition 

During the times of Social Distancing and Covid Regularization, wearing masks has been crucial.
This POC works on the concept of distingushing individuals based on if they are wearing masks or not.

# Dataset 
https://www.kaggle.com/datasets/techzizou/labeled-mask-dataset-yolo-darknet

# Darknet 
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.
Using YOLOv4 pre-trained weights and training them to identify mask wearers from those who are not wearing the masks.

# Files Required

## obj.data file
Classes = Number of classes which are to be recognized
Train text file path
Test text file path
Backup folder path

## obj.names file
Names of classes ( With_mask, Without_mask)

## Preprocess file
python file to generate the file path of train and test files

## Cfg file Changes 
- change line batch to batch=64
- change line subdivisions to subdivisions=16
- change line max_batches to (classes*2000 but not less than number of training images and not less than 6000), f.e. max_batches=6000 if you train for 3 classes
- change line steps to 80% and 90% of max_batches, f.e. steps=4800,5400
- set network size width=416 height=416 or any value multiple of 32
- change line classes=80 to your number of objects in each of 3 [yolo]-layers
- change [filters=255] to filters=(classes + 5)x3 in the 3 [convolutional] before each [yolo] layer, keep in mind that it only has to be the last [convolutional] before each of the [yolo] layers. So if classes=1 then it should be filters=18. If classes=2 then write filters=

