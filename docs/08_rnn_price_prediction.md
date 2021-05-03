## Recurrent Neural Network

### Definition

A Recurrent Neural Network (RNN) is a type of neural network well-suited to time series data. RNNs process a time series step-by-step, maintaining an internal state from time-step to time-step. In other words a recurrent neural network looks quite similar to a traditional neural network except that a memory-state is added to the neurons.

The computation to include a memory is simple.

Consider a simple model with only one neuron feeds by a batch of data. In a traditional neural net, the model produces the output by multiplying the input with the weight and the activation function. 
With an RNN, this output is sent back to itself several number of times. 

We call timestep the amount of time the output becomes the input of the next matrice multiplication.

Hyperparameters (the parameters of the model, i.e., number of neurons, etc.) for the model built on the basis of RNN are as follows:

Number of input: 1

Time step (windows in time series): 10

Number of neurons: 120

Number of output: 1

RNN is useful for an autonomous car as it can avoid a car accident by anticipating the trajectory of the vehicle. RNN is widely used in text analysis, image captioning, sentiment analysis and machine translation. For example, one can use a movie review to understand the feeling the spectator perceived after watching the movie. Automating this task is very useful when the movie company does not have enough time to review, label, consolidate and analyze the reviews. The machine can do the job with a higher level of accuracy.

### Step 0. Install keras

```
pip install keras

(test-tf) d:\repos-research\python-tensorflow>pip install keras
Collecting keras
  Downloading Keras-2.4.3-py2.py3-none-any.whl (36 kB)
Requirement already satisfied: scipy>=0.14 in c:\programdata\anaconda3\envs\test-tf\lib\site-packages (from keras) (1.6.3)
Requirement already satisfied: numpy>=1.9.1 in c:\programdata\anaconda3\envs\test-tf\lib\site-packages (from keras) (1.19.5)
Collecting pyyaml
  Downloading PyYAML-5.4.1-cp38-cp38-win_amd64.whl (213 kB)
     |██| 213 kB 3.3 MB/s
Requirement already satisfied: h5py in c:\programdata\anaconda3\envs\test-tf\lib\site-packages (from keras) (2.10.0)
Requirement already satisfied: six in c:\programdata\anaconda3\envs\test-tf\lib\site-packages (from h5py->keras) (1.15.0)
Installing collected packages: pyyaml, keras
Successfully installed keras-2.4.3 pyyaml-5.4.1
``` 

### Step 1. Load data (usually from csv)

On this stage perform necessary transformations, such as column splitting/merge, etc
Before to construct the model, you need to split the dataset into a train set and test set. The full dataset has 721 data points; we will use the first 600 point to train the model and the last 121 points to test the model.


### Step 2. Split initial data set into 2 parts: train dataset and test dataset



### Step 3. Define features and labels



### Step 4. Normalize data


### Step 5. Implementing DNN regression




### Step 6. Performance


### Step 7. Make predictions


