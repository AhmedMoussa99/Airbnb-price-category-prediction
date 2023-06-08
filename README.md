# Airbnb-price-category-prediction
Problem formulation
When hosts prepare to post a new advertisement about residence place on the Airbnb site is, how much should they ask for?, How much of this apartment?, etc, also for guests, they want to find a suitable place to stay at it affordable price..., So we want to build a neural network model to make predict the type of real estate and its price, our inputs here are summary for this real estate and its image and the outputs here are a type of this real estate and its price. (training dataset:- 7627 samples), (test dataset:- 7360 samples).

Note:- you will find the dataset at https://www.kaggle.com/competitions/cisc-873-dm-f22-a4

# Challengs:
The size of training dataset is approximately equal to test dataset and it will be smaller when we drop null and duplicated values from training dataset.
Null values in summary feature in training dataset.
summary feature in both training dataset and test dataset is multilingual.
imbalanced labels distribution.
multi-prediction problem.
huge time taken to train with cpu.
Impact:
It will help hosts to put the true and suitable price for their residence place and that will increase their sales, also it will help guests to predict the night price for the place that they are looking for it to stay in it at holidays or in the work trip days.

# Data mining function:
load the data from the source.
preprocess and manipulating the data.
build and train the model.
classification and prediction.
get insights from the results.
Ideal solution:
For me using a bert model (pre-trained model) was a great choice, it got the highest score for me on kaggle, and I think that's because a lot of learnable parameters.

Actually this model is the best model that you can use it for this kind of problems, bert model is a great semantic and that because a lot of learnable parameters, more than 108 million trainable parameters. kaggle score (68.546), and I could got better result if I tried to tune the hyperparameters of this model.

# Experimental protocol
load train and test data.
some visualization and description to understand the data.
preprocessing the data
A.preprocessing the data to build models from scratch.

a. translate text data. (summary feature).

b.remove null and duplicated values from summary feature in training dataset.

c.translate summary feature (because it's multilingual data).

d.resize images into (64643) shape (to preserve more features as we could).

e.tokenize each text data in summary feature.

f.convert each text into unique id sequence.

B.preprocessing the data to build a pre-trained model.

a.translate text data. (summary feature).

b.remove null and duplicated values from summary feature in training dataset.

c.translate summary feature (because it's multilingual data).

d.tokenize each text data in summary feature with pre-trained tokenizer.

e.convert each text into unique id sequence.

build models and plot them.
train each model.
plot each model on training loss and validation loss.
plot each model on training accuracy and validation accuracy.
