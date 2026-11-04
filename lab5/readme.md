Handwritten Digit Recognition Using LSTM
1. Program Title

Handwritten Digit Recognition using Long Short-Term Memory (LSTM)

2. Aim

To develop a Deep Learning model using LSTM (Long Short-Term Memory) to recognize handwritten digits from 0 to 9 using the MNIST dataset.

3. Dataset Used

MNIST Handwritten Digit Dataset

Total images: 70,000
Training images: 60,000
Testing images: 10,000
Image dimensions: 28 × 28 pixels
Number of classes: 10 (digits 0–9)
Pixel values: 0–255

The dataset is loaded using TensorFlow/Keras.

4. Methodology

The project involves the following steps:

Load the MNIST dataset.
Normalize pixel values to the range [0, 1].
Reshape images into 28 time steps and 28 features for LSTM input.
Convert digit labels into one-hot encoded format.
Build an LSTM model with 64 units.
Add a Dense output layer with 10 neurons and Softmax activation.
Compile the model using the Adam optimizer and categorical cross-entropy loss.
Train the model for 5 epochs with a batch size of 32.
Evaluate the model using test data.
Plot training and validation accuracy.
5. Results

The LSTM model was trained on the MNIST handwritten digit dataset for 5 epochs.

The model's performance was evaluated using test accuracy and test loss.

A graph of training accuracy and validation accuracy was plotted to observe the learning performance of the model.

Test Accuracy: Add the actual accuracy obtained after running the program.

Observation: The model learns patterns from handwritten digit images and predicts the corresponding digit from 0 to 9.

6. Technologies Used
Python
TensorFlow / Keras
NumPy
Matplotlib
MNIST Dataset
7. Conclusion

The project demonstrates how LSTM networks can be used for handwritten digit classification. The model processes image rows as sequential input and learns patterns to recognize handwritten digits.