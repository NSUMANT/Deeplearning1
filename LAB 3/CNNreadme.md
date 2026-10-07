Week 03 - CNN
Program Title

Convolutional Neural Network (CNN) for MNIST Digit Classification

Aim

To implement and train a Convolutional Neural Network (CNN) using TensorFlow/Keras for classifying handwritten digits from the MNIST dataset.

Dataset Used

MNIST Handwritten Digit Dataset

The MNIST dataset contains 60,000 training images and 10,000 test images of handwritten digits from 0 to 9. Each image has a size of 28 × 28 pixels.

Methodology

The following steps are performed in the program:

Load the MNIST dataset using TensorFlow/Keras.

Reshape the images to include a single channel.

Normalize pixel values from the range 0–255 to 0–1.

Build a CNN consisting of:

Three convolutional layers

Two max-pooling layers

A flattening layer

A dense hidden layer with 64 neurons

A final dense layer with 10 neurons using softmax activation

Compile the model using the Adam optimizer and sparse categorical cross-entropy loss.

Train the model for 5 epochs.

Evaluate the model using the test dataset.

Plot training/validation accuracy and loss.

Model Architecture

Conv2D: 32 filters, 3×3 kernel, ReLU activation

MaxPooling2D: 2×2

Conv2D: 64 filters, 3×3 kernel, ReLU activation

MaxPooling2D: 2×2

Conv2D: 64 filters, 3×3 kernel, ReLU activation

Flatten

Dense: 64 neurons, ReLU activation

Dense: 10 neurons, Softmax activation

Results

The model is trained for 5 epochs and evaluated on the MNIST test dataset. The final test accuracy is displayed by the program as:

Test accuracy: <value obtained after execution>

The accuracy and loss graphs show the training and validation performance of the CNN across the five epochs.

Conclusion

The CNN successfully learns features from handwritten digit images and performs digit classification on the MNIST dataset. The training and validation accuracy demonstrate that the model is effective for this image classification task.