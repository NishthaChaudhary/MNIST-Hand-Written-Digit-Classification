# MNIST-Hand-Written-Digit-Classification
Choosing any two digits e.g. 0 and 5 and using :

* KNN
* Gaussian NB
* Random Forest Machine Learning 
* Support Vector Machine

Classifying the data set amonf these two labels by traing the above models.

![image](https://user-images.githubusercontent.com/54689111/82743611-ba277200-9d3b-11ea-9459-62201c425ad7.png)


## Neaural Network for the Classification problem:

### Dataset:

MNIST dataset with x_train shape= (60000, 28, 28); y_train shape= (60000,); X_test shape= (10000,28,28) and y_test shape= (10000,)

### Pre-processing Dataset:

* Reshape the X_train values into 60000, 28*28
* Reshape the X_test values into 10000, 28*28
* Reshape the y values into 10 categories.
* Convert the values in the array into float
* Divide the values by 255. as we want to normalize the data.


### Build the Neural Network

The structure of the Neaural network is as below:

![image](https://user-images.githubusercontent.com/54689111/82743447-a844cf80-9d39-11ea-8100-2bf8590e3939.png)

#### Hyperparameters used:

* optimizer: adam
* loss: categoical_crossentropy
* activation for first Dense layers: relu
* activation for output layer: softmax
* epochs: 20

### Model Evaluation:

![image](https://user-images.githubusercontent.com/54689111/82743535-b2b39900-9d3a-11ea-8337-4ba2e4e11d92.png)


## Convolutional Neaural Network for CLassification Problem:

### Build the CNN Model:

![image](https://user-images.githubusercontent.com/54689111/82743556-f5757100-9d3a-11ea-9e26-3e0460653078.png)


#### Additional parameters used:

* Kernel_size: 3*3
* Max_pooling2D layer
* Flatten layer

### CNN Evaluation VS Neural Network Model Evaluation:

![image](https://user-images.githubusercontent.com/54689111/82743588-5bfa8f00-9d3b-11ea-98b7-06200393b40f.png)

### Model Enhancements:

* Include Dropout layer: Randomly kill or throw away connetions in layer of training set. Purpose is to prevent overfitting; only done on taining data.

* Image Augmentattion: Taking images that are already in the training dataset and manipulating them in order to create many altered versions of the same image. First, this method provides more images for our model to train on; Second, this manipulation method makes our model more robust.


## Implementing More Tensorflow:

Further, I have implemented TensorFLow operations, dataset manipulations and implented tensorflow estimators for Linear Regression and Neural Network.

The visualization is done using TensorBoard.
