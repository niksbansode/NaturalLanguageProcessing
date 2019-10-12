# Introduction
In this notebook, I have built a recurrent neural network that functions as part of an end-to-end machine translation pipeline. Your completed pipeline will accept English text as input and return the French translation.

English -> French translation pipeline is as follows:
1. **Preprocess** - Converted text to sequence of integers using the following preprocess methods:
	- Tokenized the words into ids
	- Added padding to make all the sequences the same length.
2. **Models** - Create models which accepts a sequence of integers as input and returns a probability distribution over possible translations.
Following RNN model strategies have been identified and ultimately combined to make a model robust for better seq2seq prediction.
	- Model 1 is a simple RNN
	- Model 2 is a RNN with Embedding
	- Model 3 is a Bidirectional RNN
	- Model 4 is an Encoder-Decoder RNN
	- Model 5 is the combination of all of the above.
	
	In the first place these models have used GRUs to solve the vanishing gradient problem of a standard RNN.
3. **Prediction** - To run the model on English text.

The final model has acheived 97.14% accuracy score.

# Setup

This project requires GPU acceleration to run efficiently.

## Install
- Python 3
- NumPy
- TensorFlow 1.x
- Keras 2.x
