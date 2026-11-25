# Bidirectional RNN for Music Generation

## Aim
To build a two-layer Bidirectional LSTM model that predicts the next note in a sequence and generates a new sequence of notes.

## Dataset Used
A synthetic dataset of 1,000 randomly generated melodies was used. Each melody contains 30 notes selected from 50 possible note tokens. The notes were one-hot encoded before training. No external music dataset was used.

## Results
The model was trained for 20 epochs and achieved approximately 96.12% validation accuracy. It generated a sequence of 50 notes and a piano-roll visualization.

However, the high accuracy does not mean that the model learned musical patterns. Because the notes are random and the model is bidirectional, its backward LSTM can access future notes during training. The generated sequence was also repetitive. A unidirectional LSTM with causal training would be more suitable for genuine next-note music generation.
