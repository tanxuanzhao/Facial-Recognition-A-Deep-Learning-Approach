# Facial Recognition - A Deep Learning Approach

**Research related to improving facial recognition models**

Final Year (Capstone) Project, University Of Wollongong, October 2023 – March 2024

The original Model uses MTCNN which has been modified to make it easier for me to test the modification of activation functionss of the CNN layers.

For the Original CNN/ MTCNN model 1 test is done with nothing changed.

For the Modified Sigmoid Model a test from the range of 10% of sigmoid value to 90% of Sigmoid value is done.

For Modified Softmax Model a test from the range of 10% sigmoid value to 90% Sigmoid value is done.

For Modified LeakReLU a test from the range of alpha 0.1 to 1 is done.

**For detailed testing results, please refer to:**

[All test results collated on an Excel Spreadsheet](https://docs.google.com/spreadsheets/d/1VRlNWW4ECAq2A-0j24l10WNPhOHGx97E/edit?pli=1&gid=434247271#gid=434247271)

The original Model uses MTCNN which has been modified to make it easier for me to test the modification of activation functions of the CNN layers. I modified the original model to test how the modification of activation fuctions such as LeakyReLU, SoftMax, Sigmoid and would affect the Accuracy, Precision, Recall and Response time of the Model. At the end of all the tests, the model with the best performance is chosen.

[Short video describing the modification of my code and what it does](https://drive.google.com/file/d/1iL_Tz7jcMc8F2qI8sTtF8x0PVAxVNYV-/view)

[Powerpoint Presenation for Project showcaseing my groups research ways to improve different facial recognition models](https://docs.google.com/presentation/d/13cZEBs54p584JNJFbSXzUMmtzN7LyOi7/edit?pli=1#slide=id.p1)
* Powerpoint showcases my group's attempts to reseach ways to improve existing Facial Recognition models
* Only work that I have done is uploaded to this repository. The whole project involves other codes and models from other group members however it is not uploaded in this repository as it is their work. 
* Previously attempted to do external modifications such as adjusting contrast and Brightness for the images parsed in for Facial Recognition and was not favorable and was rejected by the main stakeholder the Supervising Lecturer due to specification of the project to be done purely focusing on the facial recognition model itself as such modifications were done inside the model only.

&nbsp;
&nbsp;
&nbsp;


**Defintions for terms related to the project**

**Metrics:**

**Accuracy:**
Accuracy is a metric that generally describes how the model performs across all classes. It is useful when all classes are of equal importance. It is calculated as the ratio between the number of correct predictions to the total number of predictions.

**Precision:**
The precision is calculated as the ratio between the number of Positive samples correctly classified to the total number of samples classified as Positive (either correctly or incorrectly). The precision measures the model's accuracy in classifying a sample as positive.

![alt text](https://github.com/tanxuanzhao/Facial-Recognition-A-Deep-Learning-Approach/blob/main/images-for-readme./precision.PNG?raw=true)

**Precision or Recall**

The decision of whether to use precision or recall depends on the type of problem being solved. If the goal is to detect all the positive samples (without caring whether negative samples would be misclassified as positive), then use recall. Use precision if the problem is sensitive to classifying a sample as Positive in general, i.e. including Negative samples that were falsely classified as Positive.

**Recall:**
The recall is calculated as the ratio between the number of Positive samples correctly classified as Positive to the total number of Positive samples. The recall measures the model's ability to detect Positive samples. The higher the recall, the more positive samples detected.
![alt text](https://github.com/tanxuanzhao/Facial-Recognition-A-Deep-Learning-Approach/blob/main/images-for-readme./recall.PNG?raw=true)


&nbsp;
&nbsp;
&nbsp;

**Code related information:**

**Sequential model:**
A model that is built by initializing a linear stack of layers.

**Multi-task Cascaded Convolutional Neural Network (MTCNN):**
MTCNN is for Face Detection, based on TensorFlow. Implementation of the MTCNN face detector for Keras in Python3.4+. It is written from scratch, using as a reference the implementation of MTCNN from David Sandberg (FaceNet’s MTCNN) in Facenet. It is based on the paper Zhang, K et al. (2016).

**Epoch:**
An epoch is when all the training data is used at once and is defined as the total number of iterations of all the training data in one cycle for training the machine learning model. 

&nbsp;
&nbsp;
&nbsp;

**Activation functions:**

**Leaky ReLU:**
It is an activation function used in artificial neural networks to introduce nonlinearity among the outputs between layers of a neural network.

**Sigmoid:**
Sigmoid activation function, sigmoid(x) = 1 / (1 + exp(-x)). Applies the sigmoid activation function. For small values (<-5), sigmoid returns a value close to zero, and for large values (>5) the result of the function gets close to 1. Sigmoid is equivalent to a 2-element Softmax, where the second element is assumed to be zero. The sigmoid function always returns a value between 0 and 1.

**Softmax:**
The softmax function is a function that turns a vector of K real values into a vector of K real values that sum to 1. The input values can be positive, negative, zero, or greater than one, but the softmax transforms them into values between 0 and 1, so that they can be interpreted as probabilities. If one of the inputs is small or negative, the softmax turns it into a small probability, and if an input is large, then it turns it into a large probability, but it will always remain between 0 and 1. It is used as the activation for the last layer of a classification network because the result could be interpreted as a probability distribution.
