# Oil Seep Segmentation Exercise - CGG

By [Arian Gallardo](http://github.com/ariangc).

Pontifical Catholic University of Peru (PUCP).

### Table of contents
0. [Introduction](#introduction)
0. [Problem statement](#problem-statement)
0. [Solution](#solution)
0. [Results](#results)
0. [Testing statistics](#testing-statistics)

### Introduction

This repository contatins all the files that correspond to the solution of the Oil Seep Segmentation Exercise for the hiring process of the Machine Learning Engineer Internship position at CGG.

### Problem statement

In this exercise we are asked to produce a deep convolutional neural network (DCNN) and an evaluation metric to perform image segmentation on an oil seep image dataset. 

### Solution

To solve this exercise a well-known DCNN was chosen, called U-Net, which was previously described in the paper "U-Net: Convolutional Networks for Biomedical Image Segmentation" (https://arxiv.org/abs/1505.04597). This model was used in the [ISBI](https://biomedicalimaging.org/2015/) cell tracking challenge 2015, and won in these categories by a large margin. 

In addition, to measure the model performance, Dice Score and IoU (Jaccard index) were used. Both metrics are widely used in the Semantic Segmentation task of Deep Learning as they are very strong indicators of similarity between two sets of data. A combination of Binary Cross Entropy and Dice Score was used to measure the model loss.

Finally, a 70%-20%-10% dataset split ratio was used for train, validation and test sets, respectively. Image preprocessing consisted of data augmentation techniques such as horizontal/vertical flips and random rotations.

The solution was implemented in **Python** using the Deep Learning Framework **Pytorch**, as well as some third-party libraries such as OpenCV, Sklearn, etc.

### Results

0. Train and Validation Loss Curve (1000 epochs, learning rate = 0.005, optimizer = Adam)

0. Train and Validation Dice Coefficient Curve (1000 epochs, learning rate = 0.005, optimizer = Adam)

0.	Train and Validation Jaccard Coefficient Curve (1000 epochs, learning rate = 0.005, optimizer = Adam)


### Testing Statistics

* **Test Dice =  0.53089714**

* Test Jaccard (mIoU) =  0.3856979


