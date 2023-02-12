# Hand-Written-Digit-Recognisation
this project recognises a digit written by us using machine learning algorithm(ANN) 

Here's a step by step explanation:

Importing the necessary libraries: The code imports the tensorflow library as tf and the keras module from tensorflow. Keras is a high-level neural network API that provides a convenient way to build and train deep learning models.

Loading the MNIST dataset: The code uses the load_data() function from the keras.datasets module to load the MNIST dataset. The dataset is split into training and testing sets, with 60,000 images for training and 10,000 images for testing. The training set and the testing set are stored in the variables (x_train, y_train) and (x_test, y_test) respectively.

Preprocessing the data: The code normalizes the pixel values of the images by dividing each pixel value by 255.0. This is done to ensure that the pixel values are in the range [0,1] which helps to stabilize the training of the model. The code also converts the label values into one-hot encodings using the to_categorical function from the keras.utils module. This is because the output layer of the model uses a softmax activation function which requires the label values to be in the form of one-hot encodings. The code also reshapes the input data into 2D arrays with shape (-1, 28 * 28) to make it compatible with the input shape expected by the model.

Building the model: The code creates an instance of the Sequential class from the keras.models module, which represents a linear stack of layers in a neural network. The code then adds two dense layers to the model using the add method of the Sequential class. The first layer has 512 neurons and uses a relu activation function. The second layer has 10 neurons and uses a softmax activation function. The input shape of the first layer is specified as (28 * 28,) which represents the shape of the input data after it has been reshaped.

Compiling the model: The code compiles the model using the compile method and specifies the optimizer, loss function, and evaluation metric to use during training. The code uses the adam optimizer, categorical_crossentropy loss function, and accuracy metric.

Training the model: The code trains the model using the fit method and specifies the input data, target data, batch size, and number of epochs to use during training. An epoch represents one pass through the entire training set.

Evaluating the model: The code evaluates the model on the testing data using the evaluate method and prints the test accuracy.
