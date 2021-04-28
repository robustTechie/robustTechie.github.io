---
title: Part 1 - Neural Networks and Deep Learning
date:   2021-04-27 17:00:35 +0300
tags:   [deep-learning, AI, neural-network, ML, data, statistics, maths]
image: assets/img/dl_1.jpg
style: fill
color: danger
description: Introduction to Deep Learning and Neural Networks
---

## Why Deep Learning -
In the present era, as we know the whole game is changed, now if you search for a product on some e-commerce website then it fills all your mobile phone with ads related to that product. Not just this Tesla is trending now, WHY? It's because of their self-driving cars. Now you can fill your home with all those smart devices, so what just talk to them :P   

Basically, with the help of Artificial Intelligence they changed the game as electricity transformed our society 100 years ago, they changed the way things were previously. Also during this pending, we saw a lot of initiatives with various tech startups who used Deep Learning for providing some good solutions to various day-to-day problems which gave a rise to EdTech, HealthTech Startups.  

Basically, with the help of Artificial Intelligence they changed the game as electricity transformed our society 100 years ago, they changed the way things were previously. Also during this pending, we saw a lot of initiatives with various tech startups who used Deep Learning for providing some good [solutions](https://analyticsindiamag.com/11-startups-in-india-using-ai-and-robotics-to-fight-covid-19/) to various day-to-day problems which gave a rise to EdTech, HealthTech Startups.   

![]({{site.baseurl}}/assets/img/mind_nn.jpeg)   
## What is Neural Network - 
Generally, by the term Deep Learning, we mean training a Neural Network(shallow or deep). So for understanding what Neural Network is let's start with some examples. Assume that we want to convert temperature from degree C to degree Fahrenheit and we don't the actual formula which is -  F = (9/5)*C + 32   
Then it would be very hard for us to carry out this conversion. So now we'll use one magic called Machine Learning which will make the computer sit and think for the equation(y = mx + c) using input and output. So we can think of this problem something like this - 
![]({{site.baseurl}}/assets/img/nn_1.png)
So as we can see the actual equation is somewhat similar to y = mx + c. Let's some other example, more complex :)   
Assume that we need to predict the taxi fare price based on some parameters like distance covered, no. of passengers, travel time, etc etc. So let's see the basic structure for that.  
![]({{site.baseurl}}/assets/img/nn_2.png)
Okay so the above image represents a deep neural network OR maybe something could happen similar to the above-mentioned C to F conversion. What if the taxi fare just depends total distance traveled. Let's plot a graph -  
![]({{site.baseurl}}/assets/img/nn_3.png)
Let's get into some terminologies :D
- Here the Blue box, the Red Box, and the last circle (didn't put any colored box) are called layers i.e.
    1. Blue box - Layer 1
    2. Red Box - Layer 2
    3. Last circle - Layer 3 or output layer
    * Here Layer 1 and 2 are also called as Hidden Layer
- Inputs are also called as Features and Outputs as Predictions.
- Each circle is called as Neuron or Unit.  

### Using Supervised Learning in Neural Networks -
Let's take the first example where we made C to F converter. So here initially we have input and output based on that we found some linear equations and with the help of that equation and input we are going to find any output in the future. Similarly, let's the next example of predicting taxi fare there also we had some input and output, and then we found the neurons, and finally, with the help of neuron and input, we are going to find the taxi fare in the future. Similarly in various other cases like computer vision, let's say we have an image of a cat and dog so we can predict which one is can and which is not.   

So from all these examples, we can say that if we have input and output then based on that we can design the model, and then with the help of that model and input, we can find the output in the future. This is Supervised Learning. Generally, Supervised Learning maps the input to output with the help of example input-output pair the model.   
### Why sudden rise in Deep Learning? 
So why Deep Learning became popular is one more thing to discuss before diving more into neural networks. So in traditional ML algorithms, we use SVM, Logistic Regression, etc algorithms, here the main problem was on increasing the amount of data to some point the performance increases but then after that, it goes to a saturation point, and then no such significant increase in performance happens. So in traditional ML algorithms amount of data is not very important after a certain point in time.  

But now because of the evolution of Neural Networks, the amount of data is also an important parameter that has its impact on performance. For example, we are using a Large NN (NN with high numbers of layers) then they have a good relationship between the amount of Data and Performance, same goes with shallow NN (NN with less no. of the layer) but less as compared to Deep NNs.   

Also, if the amount of data is really less it completely depends on our algorithm i.e. maybe SVM could perform better as compared to NN or vice versa. But for the large amount of data DL is the best way to make predictions. So in DL we can tune performance with the help of Data, Computation, or Algorithms. Nowadays there are various like Jupyter Notebook, Google Colab, etc they provide GPU support to enable fast computation.  
