# EVA8

This has assignments from EVA 8.
Uploaded Assignment2 07-Dec-2022.

#####################################################################

Uploaded Assignment2.5 dated 06-Jan-2023.

Problem Statement
Write a neural network that can take 2 inputs:

an image from the MNIST dataset (say 5), and a random number between 0 and 9, (say 7)

and gives two outputs:

the "number" that was represented by the MNIST image (predict 5)

the "sum" of this number with the random number and the input image to the network (predict 5 + 7 = 12)

#############################################################################

Data generation strategy for the random numbers
we will generate a torch tensor with 28 columns and 28 rows with all zeros and then replace the zeros with 1s

generate an integer between 0 and 9

create a one hot encoded vector with 28 columns and 1 row with all zeros and then replace the zeros with 1s at the index of the integer

multiply the random_number with the one_hot and reshape it to a [1, 28, 28] tensor with a single channel

the mnist data strategy is same as what was used in class/prev assignment

#############################################################################

Define network
create a network with two inputs random number and MNIST image

The network is designed to operate independently of each other for each of the inputs.

The first branch consists of four convolutional layers and two max pooling layers.

The second branch consists of the same four convolutional layers and two max pooling layers.

The output of each branch is passed through a fully connected layer, and then the final output is obtained using a log softmax function.

This approach allows to idependently predict the mnist and the input random number.
This approach has given in the final epoch (epochs =5) an accuracy of
Test set: Average loss: 0.000000, MNIST_Test_Accuracy: 9917/10000 (99.17%), Random_Number_Test_Accuracy: 10000/10000 (100.00%)

#############################################################################
