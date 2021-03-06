# Sign-Language-Detection-and-Conversion-to-Text-Using-CNN-and-OpenCV
The project focuses on translating American Sign Language into text using CNN model and OpenCV library of python. The training and testing of the model will done by classical convolutional neural network and then for real time application OpenCV will be used to detect the hand gesture and then the final prediction will be made by the CNN model.
# Goals
1.  Building a classification model using CNN to classify the sign language into alphabet and other classes with maximum accuracy possible.
2.  Detecting the hand gesture using OpenCV
3.  Making real time prediction using the classification model
4.  Convert it into text for furthur use.
# Dataset
The data set is a collection of images of alphabets from the American Sign Language, separated in 36 folders which represent the various classes. The training data set contains 2515 images which are 400x400 pixels. There are 36 classes, of which 26 are for the letters A-Z and 10 are numbers 0-9.The test data set contains a mere 36 images, to encourage the use of real world test images. The Data is collected from kaggle. Link : https://www.kaggle.com/ayuraj/asl-dataset
# Preporcessing
In this phase a dark background is pasted around all the images and the images are converted to ‘RGB’ format to make the image channels similar. Next all the images are transformed to similar dimension 400x400. At the end images are saved but while saving the images extension of the images are changed to .jpeg from .png. The input of this phase is the collected image dataset and output is the processed image dataset. This is done in PreProcess.ipynb file.
# Model Training
In the second step the CNN model is trained with the images which are classified to 36 classes (A-Z and 0-9) previously. The CNN model contains total 9 layers. First two are two convolution layers followed by 1 maxpool layer. Then again two convolution layer followed by 1 maxpool layer. Then there is one flatten layer which is followed by two fully connected layer(dense). For optimizing the model “stochastic gradient descent” (SGD) method is used and the model is trained for 10 epochs. The input of the model is the preprocessed image set. And while training the model the error has been minimized as much as possible. The final result of this phase is the CNN classifier. This is done in train1.ipynb file.
# Making the Interface
The 3rd step is to make the interface that will interpret the sign language and will convert to text. This is made using OpenCV library of python. First the image of the palm gesture is captured using the webcam of the computer and preprocessed using the OpenCV tools so that it can be fed into the CNN model. The preprocessed image has been fed to the pretrained model. And the model predicts the class of that image and then the class is converted to respective alphabet or digit and is shown into the screen. The user or anyone can see that. The input of this phase is the captured signed gesture and the output is corresponding alphabet or image that is converted text. This is done in gesture_recognition.ipynb file.
# Testing
The model gives almost 99% accuracy while predicting. And the interface is quite stable enough which can detect gesture in an interval of 30 miliseconds. It can print the detected character in console and screen.
# Scope
The future plan with this project is to built a front end application i.e. an android application so that it can come in the help of people. It can be used by doctors, teachers and other people to interact with the deaf and dumb community.
# Instructions to Run
first install the required python modules using the commands
1.  pip install keras
2.  pip install tensorflow==1.4.0
3.  pip install opencv
Then run the train1.ipynb file modifying the dataset path.
After the model is built and saved to the prefered location run the gesture_recognition.ipynb file.
