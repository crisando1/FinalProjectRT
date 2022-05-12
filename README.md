# FinalProjectRT
Real-Time 4106 Final Project by Matthew Weaver, Utsang Dhungel, Cristian Sandoval, Carlos Urias

Detecting Pedestrians using Python 

Abstract— The purpose of this project is to train a Convolutional Neural Network with a dataset consisting of thousands of images of people and objects. The goal is to train the Network to be able to detect objects in new images after it has trained successfully.

I. INTRODUCTION  
Python is a coding language that is capable of processing large amounts of data very fast and effectively in order to execute certain things the programmer wants. In this case, This project will be using python to train a Convolutional Neural Network to detect pedestrians in images. This is done by training the Neural Network with a dataset that contains thousands of images of people and objects. After the training is completed, the Neural Network would be able to detect pedestrians in images it has never seen before

II. Dataset and Training Method
 For our solution, the team used a method called Detecto. Detecto is built on top of pytorch to help detect objects. It utilizes RESNET50, with pretrained weights made for computer visual purposes.  To preprocess the data for detection, a well labeled .xml file needs to also be present. The first dataset that the team tried to utilize was the Kaggle Pedestrian dataset. Unfortunately, while training Detecto with this dataset, the team discovered that the author of the dataset mismatched some of the images and .xml files resulting in an error where the training could not read a particular image. After several attempts, the team concluded that there were no datasets of pedestrians that were properly formatted for Deteco. Because of this, the team had to manually label with bounding boxes using an application called Label-Img. From this software, the team was able to produce correct result.
