---
title: Part 2 - Neural Networks and Deep Learning
date:   2021-05-15 18:01:35 +0300 
tags:   [deep-learning, AI, neural-network, Data, Maths]
image: assets/img/nn_part_2.jpeg
style: fill
color: yellow
description: Let's dive basic ML problem classification and simple Neural Network
---

Let's start our basic discussion from classificaiton of Deep Learning and Machine Learning on the basis of various learning algorithm.

![]({{site.baseurl}}/assets/img/nn_part_2.jpeg)   
## What is Machine Learning
ML basically provides a computation algorithm for making machines take decisions automatically i.e. they will take decisions without explicitly programming them. It is like machines observe a pattern and attempt to imitate it in some way.

## What is Deep Learning
Ok I know we discussed about DL in last blog but let's see it again :P.
DL is the subset of ML, it uses ANN which resembles with the human brain. It has its good application in an industrial area which sometimes involves CV, NLP, automatic speech recognition, etc..

Now let's come to the main point of this blog i.e. classification based on various learning algorithm.

### Supervised and Unsupervised ML  
**Supervised -** It is a method that transforms one dataset into other. Basically, it maps input and output, and then based on that mapping it predicts the output in the future. It is very useful in narrow AI or weak AI or applied AI. Basically, it has knobs that the algorithm adjusts to increase accuracy. 
![]({{site.baseurl}}/assets/img/nn_part2_1.png)

For example - If we know the Monday stock price of the last 10 years and map a relation of Tuesday stock price with the Monday data, then we'll be able to predict the Tuesday price based on last Monday price.

![]({{site.baseurl}}/assets/img/nn_part2_2.png)

**Unsupervised -** In the supervised learning method instead of turning a knob for the dataset, we classify the dataset into some label or class. It just finds the pattern in the data and learns from that. 

For example - Clustering a dataset into groups, a dataset which has objects like puppies, pizza, kittens, moms, etc. We can find the pattern as food or not food, cute or delicious, etc.

![]({{site.baseurl}}/assets/img/nn_part2_3.png)
### Parametric and Non-parametric ML  

**Parametric -**  It is a model which is characterized by having a fixed number of parameters.

**Non-parameteric -** In this type of model number of parameters is infinite (basically determined by data). For example - KNN, Decision tree, SVM, etc.

Now let's combine all together so we'll get four classes

**Supervised + Parametric Learning -**
Here we have a fixed number of knobs or parameters. Based on these parameters it tunes the models and then checks whether the prediction was correct or not and then further adjusts the fixed number of knobs to attain more accuracy. So it has the basic steps like - 

1. Predict 
2. Compare to the truth pattern(actual output)
3. Learn the pattern and adjust the knobs
![]({{site.baseurl}}/assets/img/nn_part2_4.png)

**Unsupervised + Parametric Learning -**
It is similar to supervised parametric learning but here we adjust the fixed knobs to arrange data into the cluster. Like we can adjust the knobs to train put data into various clusters.
![]({{site.baseurl}}/assets/img/nn_part2_5.png)

![]({{site.baseurl}}/assets/img/nn_part2_6.png)

**Supervised/Unsupervised + Non-parametetric Learning -**
It uses a flexible number of parameters, and the number of parameters often grows as it learns from more data. So in the case of *supervised* it will just increase the parameters for the labeled data and in *unsupervised* it will use this method of learning to make clusters.

Now let's dive into making a simple Neural Network :D

#### Making of the simple Neural Network
As in the last example, we saw that it is only making the prediction based on one input data point, but in typical NN it is not like that. So in order to make predictions more fruitful, we need to combine multiple inputs at the same time. It allows the network to combine various properties and information to make more informed or precise decisions. But the primary logic is the same for each datapoint i.e. NN accepts and input variable as information and weights as knowledge and output as a prediction.

![]({{site.baseurl}}/assets/img/nn_part2_7.png)
For example: In a match of cricket we can predict the win/loss by past records or in a baseball match we can predict win/loss by a number of toes before the match.

- Input data - It's the data which we recorded from the real-world somewhere, like temperature, cricket score, traffic intensity, etc.
- Prediction - With the help of input data and the weights the network will make some predictions, like from traffic records it can predict the traffic intensity on a particular day, by previous match score and player records we can predict whether the team will win or lose the match.

These predictions need to not be true every time, neural networks will learn from the mistakes and correct them. For example, if the prediction is too high then it will adjust the weight so that the prediction will be less next time.

#### Making prediction with multiple inputs
As in the last example, we saw that it is only making the prediction based on one input data point, but it is not like that in typical NN. So to make predictions more fruitful, we need to combine multiple inputs at the same time. It allows the network to combine various properties and information to make more informed or precise decisions. But the primary logic is the same for each datapoint i.e. NN accepts and input variable as information and weights as knowledge and output as a prediction.

Vectors and matrices made this game very easy, they can perform a mathematical operation in groups like sum, dot products, etc. (Fun fact: Dot product gives us a notion of similarity between two vectors)
![]({{site.baseurl}}/assets/img/nn_part2_8.png)

```
def w_sum(a,b):
	assert(len(a) == len(b))
	output = 0
	for i in range(len(a)):
	output += (a[i] * b[i])
	return output

weights = [0.1, 0.2, 0]

def neural_network(input, weights):
		pred = w_sum(input,weights)
		return pred
toes = [8.5, 9.5, 9.9, 9.0]
wlrec = [0.65, 0.8, 0.8, 0.9]
nfans = [1.2, 1.3, 0.5, 1.0]

input = [toes[0],wlrec[0],nfans[0]]
pred = neural_network(input,weights)
print(pred)
```

##### NumPy code
```
import numpy as np
weights = np.array([0.1, 0.2, 0])
def neural_network(input, weights):
		pred = input.dot(weights)
		return pred
toes = np.array([8.5, 9.5, 9.9, 9.0])
wlrec = np.array([0.65, 0.8, 0.8, 0.9])
nfans = np.array([1.2, 1.3, 0.5, 1.0])
input = np.array([toes[0],wlrec[0],nfans[0]])
pred = neural_network(input,weights)
print(pred)
```

#### Making predictions with multiple outputs
We can also make multiple predictions from one input data point, and all the precautions will be completely separate. Other things are similar to multiple inputs cases.

![]({{site.baseurl}}/assets/img/nn_part2_9.png)

#### Combining both: Multiple Input + Multiple Output
Here, we have multiple input datapoints which lead us to calculate weights or outputs. You can take two perspectives on this architecture: think of it as either three weights coming out of each input node, or three weights going into each output node. We'll go with the latter one.

It performs three independent weighted sums of input to make three separate predictions.

![]({{site.baseurl}}/assets/img/nn_part2_10.png)
#### Predictions
Sometimes we need to perform this step L number of times, where we call that network as L layered neural network. So one can assume it like the input data points can predict some results and then those will carry out the future predictions like weights or final outputs.
![]({{site.baseurl}}/assets/img/nn_part2_13.png)
```
#NumPy

import numpy as np
# toes % win # fans
ih_wgt = np.array([
				[0.1, 0.2, -0.1], # hid[0]
				[-0.1,0.1, 0.9], # hid[1]
				[0.1, 0.4, 0.1]]).T # hid[2]
# hid[0] hid[1] hid[2]
hp_wgt = np.array([
			[0.3, 1.1, -0.3], # hurt?
			[0.1, 0.2, 0.0], # win?
			[0.0, 1.3, 0.1] ]).T # sad?
weights = [ih_wgt, hp_wgt]
def neural_network(input, weights):
		hid = input.dot(weights[0])
		pred = hid.dot(weights[1])
		return pred
toes = np.array([8.5, 9.5, 9.9, 9.0])
wlrec = np.array([0.65,0.8, 0.8, 0.9])
nfans = np.array([1.2, 1.3, 0.5, 1.0])
input = np.array([toes[0],wlrec[0],nfans[0]])
pred = neural_network(input,weights)
print(pred)
```

So in next blog we'll see more about Gradient Descent....
