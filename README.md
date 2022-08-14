# self-supervised-model-ResNet18-CIFAR10-CIFAR100-SimCLR
Implemention of a ResNet18 self-supervised model for transfer learning using the SimCLR framework. The CIFAR10 and CIFAR100 datasets are used.


Steps to configure the code and data
1.	To run the training execute M21AI619_train.py
2.	To run the testing execute M21AI619_test.ipynb
3.	The training TensorBoard can be found in simclr_framework.py

Implementation Details
In order to implement the solution, the following python files have been created,
1.	get_dataset.py to download and transform the training and testing CIFAR10/100 datasets
2.	get_dataset_util.py containing helper function(s)
3.	gaussian_blur.py to apply the relevant blur settings
4.	resnet_impl.py to properly initialize the resnet18 model
5.	simclr_framework.py to implement the SimCLR framework
6.	simclr_utils.py containing helper function(s)
7.	M21AI619_train.py to train the model using all of the above code and the CIFAR10 dataset
8.	M21AI619_test.ipynb to test the model against the CIFAR10 and CIFAR100 datasets
9.	The code for M21AI619_test.ipynb has been intentionally decoupled from the rest of the implementation to avoid issues in reusing methods and parameters specifically created for training only.

Transformation and Hyperparameter Details
The below recommended image transformations have been applied,
1.	random cropping, resizing back to the original size
2.	random color distortions 
3.	random Gaussian blur sequentially
 
The hyperparameters for the training are as follows,
Batch size = 500
epochs = 4
learning rate = 3e-4
out dim = 128
seed = 1
weight decay = 0.0008
