Week 04 - Multiclass Classification on Covertype Dataset
Program Title

Multiclass Forest Cover Type Classification using a Neural Network

Aim

To implement a multiclass classification neural network from scratch for predicting forest cover types using the Covertype dataset, while handling class imbalance and evaluating the model using multiple performance metrics.

Dataset Used

Covertype Dataset

The dataset contains:

581,012 samples

54 cartographic features

7 forest cover type classes

The task is to classify each observation into one of the seven forest cover types.

Steps Performed

Imported the required Python libraries, including NumPy, Pandas, Matplotlib, and Scikit-learn.

Loaded the Covertype dataset containing 581,012 samples, 54 features, and 7 classes.

Explored the dataset and visualized the distribution of the seven target classes.

Analyzed class imbalance by calculating the ratio between the most and least frequent classes.

Extracted the 54 cartographic features and the target variable.

Converted the target labels from 1–7 to 0–6 for zero-indexed classification.

One-hot encoded the target labels into a seven-column binary matrix.

Divided the dataset into:

80% training data

10% validation data

10% testing data

Used stratified splitting to maintain similar class proportions across the training, validation, and testing sets.

Standardized the input features using StandardScaler so that the features have zero mean and unit variance.

Calculated class weights to reduce the effect of class imbalance during training.

Defined a neural network architecture with the following layers:

54 → 64 → 32 → 16 → 7

Initialized network parameters using He initialization, which is suitable for ReLU activation functions.

Implemented forward propagation using:

ReLU activation for hidden layers

Softmax activation for the output layer

Implemented weighted categorical cross-entropy loss.

Implemented backpropagation with class weights incorporated into the gradients.

Trained the network using mini-batch Stochastic Gradient Descent (SGD) with a batch size of 128.

Applied early stopping by monitoring validation loss and stopping training when there was no improvement for 15 epochs.

Generated class probabilities for the test dataset using the softmax output.

Converted predicted probabilities into class labels using argmax.

Evaluated the model using:

Accuracy

Precision

Recall

F1-score

Per-class metrics

Macro-average metrics

Generated a 7 × 7 confusion matrix to compare actual and predicted classes.

Visualized training and validation loss and accuracy curves.

Created a confusion matrix heatmap with annotations.

Plotted per-class F1-scores to compare classification performance among the seven classes.

Analyzed the precision-recall trade-off for each class.

Compared the actual class distribution with the predicted class distribution.

Neural Network Architecture
Layer	Input/Output	Activation
Input	54 features	—
Hidden Layer 1	64 neurons	ReLU
Hidden Layer 2	32 neurons	ReLU
Hidden Layer 3	16 neurons	ReLU
Output Layer	7 neurons	Softmax
Training

The model was trained using mini-batch SGD with a batch size of 128.

To address the imbalance in the Covertype classes, class weights were incorporated into the loss function and backpropagation process.

Early stopping was used based on validation loss, with a patience of 15 epochs.

Evaluation

The trained model was evaluated on the test set using accuracy, precision, recall, and F1-score.

Per-class precision, recall, and F1-score were calculated to identify classes that were easier or more difficult for the model to classify.

A 7 × 7 confusion matrix was generated to identify which forest cover types were most frequently confused with one another.

Visualizations

The following visualizations were generated:

Class distribution plot

Training and validation loss curves

Training and validation accuracy curves

7 × 7 confusion matrix heatmap

Per-class F1-score plot

Precision vs. recall comparison

True vs. predicted class distribution

Results

The model's performance was evaluated using the test dataset. The final accuracy, precision, recall, and F1-score should be recorded from the actual execution output.

Test Accuracy: <enter actual value>

Macro Precision: <enter actual value>

Macro Recall: <enter actual value>

Macro F1-Score: <enter actual value>

The confusion matrix and per-class F1-score visualization were used to identify classes where the model performed well and classes that were more difficult to distinguish.

Conclusion

A neural network was successfully implemented for multiclass forest cover type classification using the Covertype dataset. The experiment demonstrated the complete machine learning pipeline, including data exploration, preprocessing, stratified data splitting, feature standardization, class-imbalance handling, neural network training, early stopping, and comprehensive model evaluation.

The use of class weights helped address the imbalance between forest cover type classes. The confusion matrix, per-class F1-scores, and precision-recall analysis provided additional insight into the strengths and weaknesses of the classifier.