# PyTorch Library in Python Cheat Sheet 🚀🔥

Welcome to the PyTorch cheat sheet! PyTorch is an open-source deep learning platform that provides a seamless path from research prototyping to production deployment. Whether you're a beginner or an expert in deep learning, this cheat sheet will help you get started with PyTorch and includes some code examples to kick-start your deep learning journey.

## Installation

You can install PyTorch using pip:

```python
pip install torch torchvision torchaudio
```
For GPU support (if you have a compatible GPU):

```python
pip install torch torchvision torchaudio -f https://download.pytorch.org/whl/cu111/torch_stable.html
```

## Code Examples

### Creating Tensors

```python
import torch

# Create a tensor with zeros
zeros_tensor = torch.zeros(3, 3)

# Create a tensor with random values
rand_tensor = torch.rand(2, 2)

print(zeros_tensor)
print(rand_tensor)
```

### Autograd

```python
import torch

x = torch.tensor(2.0, requires_grad=True)
y = 3 * x**3 + 2

y.backward()
print(x.grad)
```

### Neural Network

```python
import torch
import torch.nn as nn

# Define a simple neural network
class Net(nn.Module):
    def __init__(self):
        super(Net, self).__init()
        self.fc1 = nn.Linear(10, 5)
        self.fc2 = nn.Linear(5, 1)

    def forward(self, x):
        x = torch.relu(self.fc1(x))
        x = self.fc2(x)
        return x

# Instantiate the network
net = Net()

# Print the network architecture
print(net)
```

### Loss Function and Optimizer

```python
import torch
import torch.nn as nn
import torch.optim as optim

# Define a simple neural network and a loss function
net = Net()
criterion = nn.MSELoss()

# Define an optimizer (SGD in this case)
optimizer = optim.SGD(net.parameters(), lr=0.01)
```

### Training a Neural Network

```python
# Loop for multiple epochs
for epoch in range(10):
    optimizer.zero_grad()  # Zero the parameter gradients
    outputs = net(inputs)  # Forward pass
    loss = criterion(outputs, labels)  # Compute the loss
    loss.backward()  # Backpropagation
    optimizer.step()  # Update weights
```

### Loading Data

```python
import torchvision
import torchvision.transforms as transforms

transform = transforms.Compose([transforms.ToTensor(), transforms.Normalize((0.5, 0.5, 0.5), (0.5, 0.5, 0.5)])
trainset = torchvision.datasets.CIFAR10(root='./data', train=True, download=True, transform=transform)
trainloader = torch.utils.data.DataLoader(trainset, batch_size=4, shuffle=True)
```

### Saving and Loading Models

```python
# Save the model
torch.save(net.state_dict(), 'model.pth')

# Load the model
model = Net()
model.load_state_dict(torch.load('model.pth'))
model.eval()
```

This cheat sheet provides an overview of PyTorch's core features and code examples to get you started. PyTorch is a powerful library for deep learning, and you can explore its extensive documentation for more advanced usage.

📖 PyTorch Documentation: [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more data science and Python-related content. Enjoy your journey into the world of deep learning with PyTorch! 🚀📊🤖
