## Linear regression

TensorFlow is equipped with a vast array of APIs to perform many machine learning algorithms. This is the high-level API. TensorFlow calls them estimators 

Low-level API: Build the architecture, optimization of the model from scratch. 

High-level API: Define the algorithm. TensorFlow provides a toolbox calls **estimator** to construct, train, evaluate and make a prediction.

Linear regression (definition)

Imagine we have two variables, x and y and the task is to predict the value of knowing the value of x. On the plot of the data, one can see a positive relationship between independent variable, x and dependent variable y.

A linear regression is evaluated with an equation. The variable y is explained by one or many covariates. In this example, there is only one dependent variable. So the equation will be:

```
y = beta + alpha * x + e
```

With:

beta is the bias. i.e. if x=0, y = beta

alpha is the weight associated to x

e is the residual or the error of the model. It includes what the model cannot learn from the data


### Step 1. Load data (usually from csv)

On this stage perform necessary transformations, such as column splitting/merge, etc

### Step 2. Split initial data set into 2(3) parts: train dataset and test dataset



### Step 3. Define features and labels

Separate the target value, the "label", from the features. This label is the value that you will train the model to predict.


### Step 4. Normalize data

It is good practice to normalize features that use different scales and ranges. 

One reason this is important is because the features are multiplied by the model weights. So the scale of the outputs and the scale of the gradients are affected by the scale of the inputs. 

### Step 5. Implementing DNN regression

The code is basically the same as in the model of linear regression for the exception that it is expanded to include some "hidden"  non-linear layers. 
The name "hidden" here just means not directly connected to the inputs or outputs.



### Step 6. Performance


### Step 7. Make predictions


