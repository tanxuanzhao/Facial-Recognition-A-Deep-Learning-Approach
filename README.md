# Facial-Recognition-A-Deep-Learning-Approach

Research related to improving facial recognition models

Final Year (Capstone) Project, University Of Wollongong, October 2023 – March 2024


This repository only contains the code and model that I used and modified from an existing model to test how the modification of LeakReLU, SoftMax, Sigmoid would affect the Accuracy, Precision, Recall and Response time of the code.

Short video describing the modification of my code and what it does
https://drive.google.com/file/d/1iL_Tz7jcMc8F2qI8sTtF8x0PVAxVNYV-/view

Powerpoint Presenation for Final Prototype of Project:
https://docs.google.com/presentation/d/13cZEBs54p584JNJFbSXzUMmtzN7LyOi7/edit?pli=1#slide=id.p1


* Powerpoint showcases my group's attempts to reseach ways to improve existing Facial Recognition models
* The project involves other codes and models from other group members however it is not uploaded in this repository as it is their work.
* Previously attempted to do external modifications such as adjusting contrast and Brightness for the images parsed in for Facial Recognition and was not favorable and was rejected by the main stakeholder the Supervising Lecturer due to specification of the project to be done purely focusing on the facial recognition model itself as such modifications were done inside the model only.

$~~~$
Defintion for terms related to the project

Metrics:

Accuracy:
Accuracy is a metric that generally describes how the model performs across all classes. It is useful when all classes are of equal importance. It is calculated as the ratio between the number of correct predictions to the total number of predictions.

Precision: 
The precision is calculated as the ratio between the number of Positive samples correctly classified to the total number of samples classified as Positive (either correctly or incorrectly). The precision measures the model's accuracy in classifying a sample as positive.

![alt text](https://github.com/tanxuanzhao/Facial-Recognition-A-Deep-Learning-Approach/blob/main/images-for-readme./precision.PNG?raw=true)

Precision or Recall
The decision of whether to use precision or recall depends on the type of problem being solved. If the goal is to detect all the positive samples (without caring whether negative samples would be misclassified as positive), then use recall. Use precision if the problem is sensitive to classifying a sample as Positive in general, i.e. including Negative samples that were falsely classified as Positive.



Recall:
The recall is calculated as the ratio between the number of Positive samples correctly classified as Positive to the total number of Positive samples. The recall measures the model's ability to detect Positive samples. The higher the recall, the more positive samples detected.
![alt text](https://github.com/tanxuanzhao/Facial-Recognition-A-Deep-Learning-Approach/blob/main/images-for-readme./recall.PNG?raw=true)

Model related information:

Sequential model:
A model that is built by initializing a linear stack of layers.


Activation functions:

Leaky ReLU:
It is an activation function used in artificial neural networks to introduce nonlinearity among the outputs between layers of a neural network.

Sigmoid:
Sigmoid activation function, sigmoid(x) = 1 / (1 + exp(-x)). Applies the sigmoid activation function. For small values (<-5), sigmoid returns a value close to zero, and for large values (>5) the result of the function gets close to 1. Sigmoid is equivalent to a 2-element Softmax, where the second element is assumed to be zero. The sigmoid function always returns a value between 0 and 1.

Softmax:
The softmax function is a function that turns a vector of K real values into a vector of K real values that sum to 1. The input values can be positive, negative, zero, or greater than one, but the softmax transforms them into values between 0 and 1, so that they can be interpreted as probabilities. If one of the inputs is small or negative, the softmax turns it into a small probability, and if an input is large, then it turns it into a large probability, but it will always remain between 0 and 1. It is used as the activation for the last layer of a classification network because the result could be interpreted as a probability distribution.
