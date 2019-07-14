# Deep_learning_MiniFramework

The objective of this project is to implement from scratch a mini deep learning framework using only PyTorch's tensor operation and the standard math library, without using autograd and neural-network modules available in PyTorch. Consists in the implementation of the forward and backward propagation implementation of several modules: Linear (fully connected layers) activation functions( Tanh, ReLU, LeakyReLU, Sigmoid), Sequential (combination of layers) and MSE (loss function) with mini batch SGD to optimize parameters. 

## Overview of the project's code

```
├── figures         <- folder with the plots of the accuracy and loss
├── README.md       <- readme of the project
├── activations.py  <- classes of the activations functions
├── benchmark.py    <- code to compare the proposed solution to the official PyTorch implementation
├── helpers.py      <- functions to generate data, convert to one hot labels, compute errors, etc.
├── linear.py       <- class linear that takes input features and output features
├── module.py       <- base class for all neural networks modules, all additional module should inherit this class
├── MSE.py          <- class of the loss function
├── report.pdf      <- report in pdf
├── sequential.py   <- class that acts as a container for different modules, stored in the order they have been passed in to the constructor
├── test.py         <- test program in .py to verify results
  
```

## Prerequisites

1. You need to have Anaconda installed, the following tutorials will guide you through the installation.

   | Operating System | Tutorial                                            |
   | ---------------- | --------------------------------------------------- |
   | Mac              | https://docs.anaconda.com/anaconda/install/mac-os/  |
   | Windows          | https://docs.anaconda.com/anaconda/install/windows/ |
   | Ubuntu           | https://docs.anaconda.com/anaconda/install/linux/   |

2. Once you have it installed, try running the following command on a terminal:

   ```
   python
   ```

   You should see a message similar to the following:

   ```
   Python 3.6.5 |Anaconda, Inc.| (default, Mar 29 2018, 13:32:41) [MSC v.1900 64 bit (AMD64)] on win32
   Type "help", "copyright", "credits" or "license" for more information.
   ```

3. Then you need to install PyTorch, try running the following command

   ```
   conda install pytorch -c pytorch
   ```

## Running the test.py

1. If your terminal is not in the location of the project files, change your directory to that location.

   ```
   cd {path_of_project_files}
   ```

2. Run the run.py script in the terminal.

   ```
   python test.py
   ```

   The program will start generating data and dividing it into train and test, next:

   * Will standardize the data (xavier initialization)
   * Build a network of 3 hidden layers (ReLU-ReLU-ReLU) and at the end use Tanh, with 2 input channels and 25 hidden units
   * Train for 250 epochs with a learning rate of 0.05

For a detailed explanation please review the report.pdf file. 