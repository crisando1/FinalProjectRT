# FinalProjectRT
Real-Time 4106 Final Project by Matthew Weaver, Utsang Dhungel, Cristian Sandoval, Carlos Urias

Detecting Pedestrians using Python 
 
Matthew Weaver, Utsang Dhungel, Cristian Sandoval, Carlos Urias. University of North Carolina at Charlotte 

Abstract— The purpose of this project is to train a Convolutional Neural Network with a dataset consisting of thousands of images of people and objects. The goal is to train the Network to be able to detect objects in new images after it has trained successfully.
I. INTRODUCTION  
Python is a coding language that is capable of processing large amounts of data very fast and effectively in order to execute certain things the programmer wants. In this case, This project will be using python to train a Convolutional Neural Network to detect pedestrians in images. This is done by training the Neural Network with a dataset that contains thousands of images of people and objects. After the training is completed, the Neural Network would be able to detect pedestrians in images it has never seen before
II. Dataset and Training Method
 For our solution, the team used a method called Detecto. Detecto is built on top of pytorch to help detect objects. It utilizes RESNET50, with pretrained weights made for computer visual purposes.  To preprocess the data for detection, a well labeled .xml file needs to also be present. The first dataset that the team tried to utilize was the Kaggle Pedestrian dataset. Unfortunately, while training Detecto with this dataset, the team discovered that the author of the dataset mismatched some of the images and .xml files resulting in an error where the training could not read a particular image. After several attempts, the team concluded that there were no datasets of pedestrians that were properly formatted for Deteco. Because of this, the team had to manually label with bounding boxes using an application called Label-Img. From this software, the team was able to produce correct results
III. Detecto Results
The results obtained from testing this Convolutional Neural Network were optimal. The main issue with this method of detection is overlapping of boxes. This was fixed almost entirely with adjusting the threshold of the object detection. The results the team obtained are shown in figure 1 and 2

Figure 1: detection of a person

Figure 2: testing with no pedestrian
While training, the team also obtained a Loss graph to show how accurate the training became over time. The graph is seen below in Figure 3.

Figure 3: Loss Graph
These results are sufficient enough to conclude this project. But the team was concerned with the issue of overbound boxes. This was most likely caused by the training dataset being very small, due to the fact that we had to manually create it. Because of this, the team decided to look for another solution for this project.
IV: Alternative Method: YOLOv5
The alternative method the team developed for this project used is YOLOv5. Using Google Colab, this method was able to detect both pedestrians, and cars in videos instead of images. After detecting a car or pedestrian, the model would create a red box around the figure, showing the object detected as well as labeling it. This particular model only had two options to classify the object as: pedestrian or car. The team saw this as a great opportunity as an alternative solution. The dataset still needed to be trained using a custom dataset, and YOLOv5 has extra dependencies  that needed to be installed. After training with a custom data set, results were obtained with this method.

V: YOLOv5 Results
Due to the established datasets being deemed faulty, the team created a custom training set of 30 images of pedestrians walking through crosswalks taken randomly from the internet. This was done to avoid the hassle of creating a large dataset from scratch. The validation set consisted of 10 images, also randomly selected from the internet. Facing the same problem as the original Detecto dataset, the annotations for each image had to be manually created in order for the training to work. The training was done with 60 Epochs and took 3-10 minutes to train. The results varied due to training being performed with a free GPU from Google Colab. Due to storage constraints, only 2 batches were used to train the model. After training, the accuracy was found to be 68%. This percentage is low due to the amount of images YOLOv5 was trained with. Although the accuracy was disappointing, the results were promising. The model was able to clearly detect the objects in the video. The results of this method of training can be viewed by going to the following youtube link:
https://www.youtube.com/watch?v=4vhj8dasQmI

Figure 4: Example of Training Set

Figure 5: Loss Graphs for Yolov5 Training

Figure 6: Example of Car Being Detected

Figure 7: Example of Person Being Detected

Figure 8: Cars and Pedestrians in the Same Frame

Figure 9: Detection from a News Feed
VI: Lessons Learned
While the team was working on this project, many different methods were tried that resulted in a very large amount of issues. These issues ranged from: Version mismatches, Unsuccessful building of certain networks, Installers failing to install required data, Installers uninstalling graphics drivers and not reinstalling them, overfitting of boxes, and label mismatching. Each of these obstacles were hurdles the team had to jump over in order to complete this project.

VII: Conclusion
After all the errors, training, and results we obtained with the several different methods attempted, the team was successfully able to detect pedestrians in images, and also able to detect cars and pedestrians from a video. The only issues with the current results is some small overfitting in the image detection, and a label mismatch in the video detection.
