# Capstone-Project-2
# Introduction
The diagnosis of pneumonia on CXR is complicated because of a number of other conditions in the lungs such as fluid overload, bleeding, volume loss, lung cancer. In addition, clinicians are reading high volumes of images every shift. Sometimes being tired or distracted clinicians can miss some details in image. Pneumonia detection using deep learning can help the clinicians to diagnose the disease

# Data
I used the dataset of Chest X-Ray Images (Pneumonia) from kaggle. It is https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia.
The Dataset includes three folders which are test, train, val. In addition, each folder includes two sub folders which are ‘normal’ and ‘pneumonia’.

# Model
I built a CNN(convolutional neural network) model.

I used five convolutional blocks with convolutional layers and max-pooling.

I used a flatten layer and followed it by fully connected layers.

Also I have used dropout to reduce overfitting.

Activation function was Relu throughout except for the last layer where it was Sigmoid as this is a binary classification problem.

I have used RMSprob as the optimizer and cross-entropy as the loss.
Before training the model I define some callbacks which are ModelCheckpoint and EarlyStopping.
# Transfer Learning
I applied transfer learning with two models which are VGG16, VGG19, InceptionV3, ResNet50 and I got best result with the model ResNet50.

# Best Model's Results
Accuracy of the model is 0.93

Recall of the model is 0.98

Precision of the model is 0.91

f1_score of the model is 0.94

The accuracy means the fraction predicted correctly to total data.

The recall means “What percent of the positive cases did you catch?”

The precision means “What percent of your predictions were correct?”

The f1-score is the harmonic mean between precision & recall. It means “What percent of positive predictions were correct? “
# Conclusion
I used a CNN model from scratch and transfer learning models which are VGG16, VGG19, InceptionV3, ResNet50. The best model was the model ResNet50 which has good accuracy which is 93% to detect pneumonia disease.
