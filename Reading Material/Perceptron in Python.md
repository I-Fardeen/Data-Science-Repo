# Creating a Perceptron in Python Cheat Sheet 🚀🧠

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Perceptrons, the simplest form of neural networks! This cheat sheet will guide you through creating and training a Perceptron in Python from scratch. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and programming insights! 🙌

## Table of Contents 🗒️

1. [Introduction to Perceptrons](#introduction-to-perceptrons)
2. [The Perceptron Algorithm](#the-perceptron-algorithm)
3. [Creating a Perceptron Class](#creating-a-perceptron-class)
4. [Training a Perceptron](#training-a-perceptron)
5. [Making Predictions](#making-predictions)
6. [Error Handling](#error-handling)
7. [Resources](#resources)

## 1. Introduction to Perceptrons 🧠

A Perceptron is a simple binary classification algorithm that mimics a biological neuron. It's a fundamental building block of neural networks and can learn to make decisions based on input data.

## 2. The Perceptron Algorithm 🔄

The Perceptron algorithm is based on the concept of a weighted sum of inputs, followed by an activation function. It's trained to adjust its weights and bias to make accurate predictions.

## 3. Creating a Perceptron Class 🐍

Create a Perceptron class in Python:

```python
class Perceptron:
    def __init__(self, num_inputs):
        # Initialize weights and bias
        self.weights = [0] * num_inputs
        self.bias = 0

    def predict(self, inputs):
        # Compute the weighted sum
        weighted_sum = sum(w * x for w, x in zip(self.weights, inputs))
        
        # Apply the activation function (e.g., step function)
        if weighted_sum + self.bias >= 0:
            return 1
        else:
            return 0
```

## 4. Training a Perceptron 🎯

Train the Perceptron to learn from data:

```python
def train(self, training_data, epochs, learning_rate):
    for _ in range(epochs):
        for inputs, target in training_data:
            prediction = self.predict(inputs)
            error = target - prediction
            
            # Update weights and bias
            for i in range(len(self.weights)):
                self.weights[i] += learning_rate * error * inputs[i]
            self.bias += learning_rate * error
```

## 5. Making Predictions 📊

Use the trained Perceptron to make predictions:

```python
perceptron = Perceptron(num_inputs)
perceptron.train(training_data, epochs, learning_rate)

# Make predictions
result = perceptron.predict(new_data)
```

## 6. Error Handling 🐞

Handle exceptions that may occur during Perceptron operations:

```python
try:
    # Perceptron code here
except Exception as e:
    print(f"An error occurred: {e}")
```

## 7. Resources 📚

Explore more about Perceptrons and neural networks:

- [Perceptron Algorithm](https://en.wikipedia.org/wiki/Perceptron)
- [Artificial Neural Networks](https://en.wikipedia.org/wiki/Artificial_neural_network)

Start your journey into neural networks by creating and training a Perceptron in Python!

Happy learning and building! 🚀🧠

Made with :heart: by **Fardeen Ahmad Khan**
