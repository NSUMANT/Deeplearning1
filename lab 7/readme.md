# Lab 7 -- Text Classification Using Bidirectional LSTM

## Aim

To build and evaluate Bidirectional LSTM models for text classification
using word embeddings. The lab demonstrates binary sentiment
classification and multi-class topic classification.

## Datasets Used

-   **IMDB Movie Reviews:** Used to classify movie reviews as positive
    or negative (2 classes).
-   **Reuters Newswire:** Used to classify news articles into 46
    different topics.

Both datasets are available through TensorFlow Keras datasets.

## Results

The IMDB model uses an Embedding layer, a Bidirectional LSTM, Dropout,
and a sigmoid output layer for binary sentiment classification. The
Reuters model uses a similar architecture with a 46-unit softmax output
layer for multi-class topic classification.

The notebooks evaluate the models using test accuracy and display
training and validation loss/accuracy plots. The IMDB task is expected
to achieve approximately 86--88% accuracy, while the Reuters task is
expected to achieve approximately 65--72% accuracy. Actual results may
vary depending on training.
