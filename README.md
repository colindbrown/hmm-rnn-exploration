# Exploration of Sequence Modeling to predict DNA Methylation

Sequence models like HMMs and RNNs provide a natural way of modelling the sequential dependence of how methylation at certain positions along the genome affects methylation at later positions. This exploration looks at the implementation and performance of variations of each type of model for predicting methylation from single-celled bisulphite sequencing data.

Viewing the files in Google Colab looks much nicer, so just click the Colab link at the top of each file

## HMM_exploration

This notebook is an implementation of a Hidden Markov Model that uses a binomial likelihood to predict methylation at a given position along the genome near a CpG island. It uses the Baum-Welch expectation-maximization algorithm to train the HMM, and visualizes the learned emission and transition matrices as well as the predicted methylation along the genome around a specific CpG island.

## RNN_exploration

This notebook manually implements a RNN model with some GRU-like gating to predict methylation at a given position from the positions before it (one-step-ahead prediction). It also compares this implementation with PyTorch's built in RNN, GRU, and LSTM layers, which all end up giving similar accuracy for the same data (although they train much faster).

## Credit
This exploration was inspired by an assignment from the Fall 2019 Columbia seminar COMS 4995_006 Machine Learning for Functional Genomics. The data comes from the DeepCpG paper [here](https://www-nature-com.ezproxy.cul.columbia.edu/articles/nmeth.3035).
