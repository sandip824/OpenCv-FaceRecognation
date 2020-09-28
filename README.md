# Real-Time Face Detection and Recognition

This project was done with “Open Source Computer Vision Library”, the OpenCV. The main focus is to impliment real time face detection system with OpenCv Python.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install packages mentioned in requirment.txt.

```bash
pip install -r requirment.txt
```

## Implimentetion Steps

To create a complete project on Face Recognition, we must work on 3 very distinct phases:

![Figure](figures/network.png)

#### 1. Face Detection and Data Gathering
The basic tas of face recognation is to detect the face from the video feed.The most common way to detect a face (or any objects), is using the “Haar Cascade classifier”.

Object Detection using Haar feature-based cascade classifiers is an effective object detection method. It is a machine learning based approach where a cascade function is trained from a lot of positive and negative images. It is then used to detect objects in other images.
Here we will work with face detection. Initially, the algorithm needs a lot of positive images (images of faces) and negative images (images without faces) to train the classifier.we cab  train your own classifier for any object like car, planes etc. you can use OpenCV to create one. 
If you do not want to create your own classifier, OpenCV already contains many pre-trained classifiers for face, eyes, smile, etc. Those XML files can be download from haarcascades directory.
##### Data Gathering
use face_dataset.py to collect the dataset to train the classifier on your datsset. enter the id of the person and it will save the some face samples with the id name as the file name. you can chnage the count of saved frames if yoy want.

#### 2. Train the Recognizer
The OpenCV Recognizer is trained on all the data collected . This is done directly by a specific OpenCV function. The result will be a .yml file that is saved in  “trainer/” directory.
use face_training.py file to train the recognizer the results will be saved as trainer.yml ib trainer directory.
#### 3. Face Recognition
the final phase  is to recognize the face.we will capture a fresh face on our camera and if this person had his face captured and trained before, our recognizer will make a “prediction” returning its id and an index, shown how confident the recognizer is with this match.




## Credits
This project uses Open Source components. You can find the source code of their open source project along with license information below. We acknowledge and are grateful to these developers for their contributions to open source.

Project: OpenCV-Face-Recognition https://github.com/Mjrovai/OpenCV-Face-Recognition
tutorial:https://towardsdatascience.com/real-time-face-recognition-an-end-to-end-project-b738bb0f7348

