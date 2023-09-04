# TensorFlow.Keras in Building Machine Learning Models 🧠🤖

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of machine learning with TensorFlow and Keras! 🚀 In this cheat sheet, we'll explore the essentials of building powerful machine learning models using TensorFlow.Keras. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more insightful content and updates! 🙌

| Topic                                | Description                                           |
|--------------------------------------|-------------------------------------------------------|
| **Introduction to Keras**            | A brief overview of Keras, a high-level neural networks API. |
| **Installing TensorFlow and Keras**  | Steps to install TensorFlow and Keras on your machine. |
| **Loading Data**                     | How to load and preprocess data for machine learning. |
| **Creating a Sequential Model**      | Building a basic sequential model using Keras. |
| **Adding Layers**                    | Adding different types of layers to your model, such as Dense and Convolutional layers. |
| **Compiling the Model**              | Configuring the model for training with optimizers, loss functions, and metrics. |
| **Training the Model**               | Training the model on your data using the `fit` method. |
| **Evaluating the Model**             | Assessing the model's performance with evaluation metrics. |
| **Making Predictions**               | Using the trained model to make predictions on new data. |
| **Saving and Loading Models**        | How to save and load your trained models for future use. |
| **Custom Layers and Models**         | Creating custom layers and models to suit your specific needs. |
| **TensorBoard Visualization**        | Visualizing model training and performance with TensorBoard. |
| **Hyperparameter Tuning**            | Techniques for optimizing your model's hyperparameters. |
| **Transfer Learning**                | Leveraging pre-trained models for your own tasks. |
| **Deployment Strategies**            | Approaches to deploy your machine learning models in real-world applications. |

Certainly, I can provide a brief explanation and code examples for each of the topics in the cheat sheet "TensorFlow.Keras in Building Machine Learning Models."

1. **Introduction to Keras**:
   - Explanation: Keras is an open-source high-level neural networks API written in Python. It's commonly used for building and training deep learning models.
   - Code Example:

   ```python
   import tensorflow as tf
   from tensorflow import keras

   # Create a sequential model
   model = keras.Sequential()
   ```

2. **Installing TensorFlow and Keras**:
   - Explanation: You need to install TensorFlow and Keras on your machine to use them. You can install them using pip.
   - Code Example: Run this command in your terminal.

   ```bash
   pip install tensorflow
   ```

3. **Loading Data**:
   - Explanation: Loading and preprocessing data is a crucial step. You can use libraries like NumPy or pandas to load and manipulate data.
   - Code Example:

   ```python
   import numpy as np
   (x_train, y_train), (x_test, y_test) = keras.datasets.mnist.load_data()
   ```

4. **Creating a Sequential Model**:
   - Explanation: The Sequential model is a linear stack of layers. You can add layers one by one.
   - Code Example:

   ```python
   model = keras.Sequential([
       keras.layers.Dense(64, activation='relu', input_shape=(784,)),
       keras.layers.Dense(10, activation='softmax')
   ])
   ```

5. **Adding Layers**:
   - Explanation: You can add various types of layers, like Dense and Convolutional, to your model.
   - Code Example:

   ```python
   model.add(keras.layers.Conv2D(32, kernel_size=(3, 3), activation='relu'))
   model.add(keras.layers.MaxPooling2D(pool_size=(2, 2)))
   ```

6. **Compiling the Model**:
   - Explanation: Before training, you need to compile the model, specifying loss, optimizer, and metrics.
   - Code Example:

   ```python
   model.compile(optimizer='adam',
                 loss='sparse_categorical_crossentropy',
                 metrics=['accuracy'])
   ```

7. **Training the Model**:
   - Explanation: Use the `fit` method to train the model on your data.
   - Code Example:

   ```python
   model.fit(x_train, y_train, epochs=5, batch_size=32)
   ```

8. **Evaluating the Model**:
   - Explanation: Evaluate the model's performance on a test dataset using evaluation metrics.
   - Code Example:

   ```python
   test_loss, test_acc = model.evaluate(x_test, y_test)
   print(f'Test accuracy: {test_acc}')
   ```

9. **Making Predictions**:
   - Explanation: Use the trained model to make predictions on new data.
   - Code Example:

   ```python
   predictions = model.predict(x_new_data)
   ```

10. **Saving and Loading Models**:
    - Explanation: You can save your trained model to disk and load it for future use.
    - Code Example:

    ```python
    model.save('my_model.h5')
    loaded_model = keras.models.load_model('my_model.h5')
    ```

11. **Custom Layers and Models**:
    - Explanation: You can create custom layers and even custom models to suit your specific needs.
    - Code Example:

    ```python
    class MyLayer(keras.layers.Layer):
        def __init__(self, output_dim, **kwargs):
            super(MyLayer, self).__init__(**kwargs)
            self.output_dim = output_dim

        def build(self, input_shape):
            self.kernel = self.add_weight(name='kernel',
                                         shape=(input_shape[1], self.output_dim),
                                         initializer='uniform',
                                         trainable=True)

        def call(self, inputs):
            return tf.matmul(inputs, self.kernel)

    ```

12. **TensorBoard Visualization**:
    - Explanation: Use TensorBoard for visualizing model training and performance.
    - Code Example:

    ```python
    tensorboard_callback = keras.callbacks.TensorBoard(log_dir='./logs')
    model.fit(x_train, y_train, epochs=5, batch_size=32, callbacks=[tensorboard_callback])
    ```

13. **Hyperparameter Tuning**:
    - Explanation: Optimize your model's hyperparameters for better performance.
    - Code Example:

    ```python
    from sklearn.model_selection import GridSearchCV
    from tensorflow.keras.wrappers.scikit_learn import KerasClassifier

    def create_model(optimizer='adam'):
        # Create and compile the model with specified hyperparameters
        # ...

    model = KerasClassifier(build_fn=create_model, epochs=10, batch_size=32)
    param_grid = {'optimizer': ['adam', 'sgd']}
    grid = GridSearchCV(estimator=model, param_grid=param_grid)
    ```

14. **Transfer Learning**:
    - Explanation: Transfer learning involves using pre-trained models for your tasks.
    - Code Example:

    ```python
    base_model = keras.applications.MobileNetV2(weights='imagenet',
                                                include_top=False,
                                                input_shape=(224, 224, 3))
    
    # Add your custom layers on top of the pre-trained model
    # ...
    ```

Made with :heart: by **Fardeen Ahmad Khan**
