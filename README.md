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
The first task is to preprocess the images. In order to do so first a background of dark is pasted around all the images and the images are converted to ‘RGB’ format to make the image channels similar. Next all the images are transformed to similar dimension 400x400. At the end images are saved but while saving the images extension of the images are changed to .jpeg from .png.
# Training
In the second step the CNN model is trained with the images which are classified to 36 classes (A-Z and 0-9) previously. The CNN model contain total 9 layers. First two are two convolution layers followed by 1 maxpool layer. Then again two convolution layer followed by 1 maxpool layer. Then there is on flatten layer which is followed by two fully connected layer(dense). For optimizing the model stochastic gradient descent(SGD) method is used and the model is trained for 10 epochs. The model is giving almost 99% accuracy.
# Gesture Recognition and prediction
The hand images has been captured by webcam using opencv library and then the captured images are fed into the pre trained models. And the predicted outcome has been printed in the output screen and console.
