# Neural Networks using Python Cheat Sheet 🧠🐍

Made with :heart: by 

Welcome to the fascinating world of Neural Networks in Python! This cheat sheet is your ultimate guide to understanding and implementing Neural Networks for various machine learning tasks. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and Data Science insights! 🙌

## 🌟 **1. Artificial Neurons**:
   - **Building Blocks**: Neurons mimic the functioning of biological neurons.
   - **Activation Functions**: Sigmoid, ReLU, Tanh.

## 🧪 **2. Feedforward Neural Network (FNN)**:
   - **Architecture**: Input layer, hidden layers, output layer.
   - **Training**: Backpropagation and gradient descent.
   
## 🌐 **3. Convolutional Neural Network (CNN)**:
   - **Purpose**: Image and spatial data analysis.
   - **Layers**: Convolutional, Pooling, Fully Connected.
   
## 🔍 **4. Recurrent Neural Network (RNN)**:
   - **Purpose**: Sequence data, time series, and natural language processing.
   - **Layers**: Recurrent, LSTM, GRU.

## 🌌 **5. Deep Learning Frameworks**:
   - **Popular Libraries**: TensorFlow, Keras, PyTorch.
   
## 🧬 **6. Building a Neural Network**:
   - **Import Libraries**:

   ```python
   import tensorflow as tf
   from tensorflow import keras
   ```

   - **Create a Model**:

   ```python
   model = keras.Sequential([
       keras.layers.Dense(128, activation='relu', input_shape=(input_shape,)),
       keras.layers.Dropout(0.2),
       keras.layers.Dense(10, activation='softmax')
   ])
   ```

   - **Compile and Train**:

   ```python
   model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['accuracy'])
   model.fit(X_train, y_train, epochs=10)
   ```

## 🔑 **7. Hyperparameter Tuning**:
   - Adjust learning rate, batch size, and network architecture for optimal performance.
   
## 🎓 **8. Transfer Learning**:
   - Reuse pre-trained models for new tasks using techniques like fine-tuning.

## 📈 **9. Model Evaluation**:
   - Metrics: Accuracy, precision, recall, F1-score.
   - Confusion Matrix and ROC curves.

## 📦 **10. Deployment and Serving**:
  - Deploy models using frameworks like TensorFlow Serving or Flask for web applications.

With this Neural Networks cheat sheet, you're ready to dive into the world of deep learning and tackle complex machine learning challenges! 🧠🐍

Made with :heart: by **Fardeen Ahmad Khan**
