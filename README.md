# Classifying Rock-Paper-Scissor Image Using Convolutional Neural Network

## Introduction
Constructing a convolutional neural network model that can detect and predict hand images. The data used includes hand data in the form of rock, paper and scissors. TensorFlow Keras was used to create a neural network for the model.

## Exploratory Data Analysis & Data Processing
Data cleaning was not carried out because the data used was quite clean (no irrelevant data in the context of rock, paper, scissors hand drawings). In order to increase the variance in the data, however, an augmentation stage is also carried out on the image by rotating it. Then the next step is to separate the data into a training set and a validation set for each image category in the rock, paper and scissors image data.

## Modelling & Evaluation
Then a model is created with a neural network which has the following architecture:
- The input layer is 300x200x3 (images of 300x200 dimensions with 3 color channels representing RGB).
- Convolutional layer 1 uses a 3x3 kernel, 32 filters, and employs the ReLU activation function.
- MaxPooling 2D layer with a pooling size of 2x2.
- Convolutional layer 2 uses a 3x3 kernel, 64 filters, and employs the ReLU activation function.
- MaxPooling 2D layer with a pooling size of 2x2.
- Convolutional layer 3 uses a 3x3 kernel, 64 filters, and employs the ReLU activation function.
- MaxPooling 2D layer with a pooling size of 2x2.
- Convolutional layer 4 uses a 3x3 kernel, 128 filters, and employs the ReLU activation function.
- MaxPooling 2D layer with a pooling size of 2x2.
- Transition to a 1-dimensional representation using the flatten function.
- Enter a fully connected layer 1 with 4096 nodes and the ReLU activation function.
- Enter a fully connected layer 2 with 2048 nodes and the ReLU activation function.
- Lastly, proceed to the output layer with 3 nodes, utilizing the softmax activation function for the classification of rock-paper-scissors images
  
The model was then trained using each piece of training data for a total of 28 epochs. The accuracy and losses of model modifications are then provided clearly as assessment and evaluation material in the training and validation process. Finally, the model is used to predict new image data. In addition, the resulting model is able to correctly predict the shape of the uploaded hand data.


