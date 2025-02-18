# ISPR

## Midterm 1

### Assignment 2

Consider the following dataset: https://www.kaggle.com/datasets/imsparsh/single-chestmounted-accelerometer

It contains accelerometer timeseries for 15 participants performing 7 different physical activities.

For this assignement focus on a single activity (of your choice) and consider the 15 participants (timeseries) you have. Your goal is to see if there are similarities and differences in the behaviour of the accelerometers of these 15 participants. In other words, you need to see how they cluster. To achieve this goal,  you can use one of the techniques we have seen during the lecture, e.g.:
- Fit an autoregressive (ARMA) model for each participant and then compare them based on the values of their ARMA coefficients (alpha and beta values)
- Transform the timeseries in the Fourier domain and compare them on their power spectrum
- ... any other thing that makes sense ...
You don't need to do the actual clustering with a clustering algorithm, as soon as you can discuss similarities and differences of the "profiles" you have constructed.

Hint: If you opt for the autoregressive analysis, you can use the autoregressive model of your choice (AR, ARMA, ...). In Python, use the ARIMA class of the statsmodels library (e.g. set order=(3,0,0) for an AR of order 3); in Matlab you can use the ar function to fit the model and the forecast function to test.

## Midterm 2

### Assignment 1

Consider the following dataset: https://archive.ics.uci.edu/dataset/360/air+quality

Fit an Hidden Markov Model to the data: it is sufficient to focus on a single column of the dataset of your choice (i.e. choose one of the sensors available and focus on analysis that single sensor). Experiment with training  HMMs with two different choices of the emission distribution and confront the results.  Experiment also with HMMs with a varying number of hidden states (e.g. at least 2, 3 and 4) and identify what is the best choice according to your own reasoning. 

Once you have identified the best HMM configuration (emissions and number of states), choose a reasonably sized subsequence (e.g. last 25% of the timeseries) and compute the optimal assignement using two methods: i) Viterbi (true optimal) and ii) best state according to the hidden state posterior (very local decision). Then plot the timeseries data highlighting (e.g. with different colours) the hidden state assigned to each timepoint by the Viterbi algorithm and the posterior method.  Discuss the results.

## Midterm 3

### Assignment 3

Consider the following dataset: https://archive.ics.uci.edu/dataset/360/air+quality

Train a neural network for sequences of your choice (LSTM, GRU, Convolutional, Clockwork RNN, ...) to predict the Benzene (C6H6 column) based on the sensor measurements timeseries (PT08.* columns) being fed in input to the recurrent model. Evaluate the predictive accuracy of the network on the task (using appropriately training/validation splits).  Confront the perfomance of this model, with another recurrent neural network trained to predict benzene one-step-ahead, i.e. given the current benzene measuement, predict its next value.
Show and compare performance of both settings.

## Midterm 4

This midterm is based on reading and summarizing the main findings of a paper.

Students are expected to deliver a short presentation (no more than 8 slides) covering the following content:
1. Introduction to the problem
2. Model description
3. Key catch of the model, represented by a commented equation
4. Key (empirical) result
5. Comment on novelties, strong points and weaknesses

Particular attention will be paid to the technical depth and understanding of the paper, which needs to be conveyed through point 3 above.

**Chosen Paper**: Junyoung Chung, Sungjin Ahn, Yoshua Bengio, *"Hierarchical Multiscale Recurrent Neural Networks"*, ICLR 2017.
