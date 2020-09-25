<h1 align="center">Malaria Detection</h1>

## Malaria Detection With Deep Learning
The goal of this kernel is to build a model that can detect malaria parasites in a cell image. The model will analyze a segmented red blood cell image and classify it as either "uninfected" or "parasitized". Once trained the model will be deployed online as a Tensorflow.js web app.

Malaria diagnosis is currently a manual process. This prototype app is capable of automatically batch analyzing cell images. Therefore, it can help speed up a doctor's diagnostic workflow and reduce diagnostic errors. It can also help medical staff to triage patients by allowing them to quickly assess the severity of each patient's infection.

We will do basic EDA, build a Keras cnn model, do 5 fold cross validation, train the model using all the data and finally evaluate the model on a holdout set.

<img src= "https://github.com/kapilahuja11/Malaria_Detection/blob/master/Assets/children.jpg" height=500 width=1000>

## :innocent: Domain Knowledge

1. Malaria is a disease that infects and destroys red blood cells.
2. Doctors analyze thick and thin blood smears to diagnose malaria and determine how severe it is.
3. The parasite that causes malaria is called Plasmodium.
4. The female Anopheles mosquito is the only mosquito that transmits malaria.

## :hourglass: EDA Summary

1. There are 27,558 segmented cell images.
2. Each folder contains 13,779 images.
3. The images are of various sizes.
4. All images are in png format.
5. All images have 3 channels i.e. all are colour images.
6. There are no all black or all white images.
7. The target distribution is balanced i.e. each target class has the same number of images.
8. All cells were segmented from thin blood smear slides.
9. The parasite specie on all parasitized images is P. falciparum.
10. Each folder contains a non image file called Thumbs.db.
11. The presence of a blue-ish area inside the cell appears to be a common (but not definitive) indicator that a cell is parasitized.

## :star: Train-Test-Split Model

1. Quickly get a feel for what kind of performance we can expect from this data.
2. Quickly test different architectures and parameters.
3. Establish the workflow that will later be used in cross validation.
4. Check the training curves to see if the model is overfitting.
5. Check the training curves to establish the number of epochs we will use when training the final model on all data.
6. Perform error analysis.

## :bulb: Create the Model Architecture

Convolution neural networks are special type of neural networks used in images recognition, images classifications and Objects detections.A convolutional neural network consists of an input and an output layer, as well as multiple hidden layers. The hidden layers of a CNN typically consist of convolutional layers, RELU layer i.e. activation function, pooling layers, fully connected layers and normalization layers.

Convolutional layer is core building block of CNN, it helps with feature detection.

Kernel K is a set of learnable filters and is small spatially compared to the image but extends through the full depth of the input image.

An easy way to understand this is if you were a detective and you are came across a large image or a picture in dark, how will you identify the image?

You will use you flashlight and scan across the entire image. This is exactly what we do in convolutional layer.

Kernel K, which is a feature detector is equivalent of the flashlight on image I, and we are trying to detect feature and create multiple feature maps to help us identify or classify the image.

we have multiple feature detector to help with things like edge detection, identifying different shapes, bends or different colors etc.

<img src= "https://github.com/kapilahuja11/Malaria_Detection/blob/master/Assets/CNN.jpeg" height=500 width=1000>

## :key: Results

<img src= "https://github.com/kapilahuja11/Malaria_Detection/blob/master/Assets/Results.png" height=300 width=600>






