#**Objective**

    Write a single model.py file that includes GN/LN/BN and takes an argument to decide which normalization to include

    Write a single notebook file to run all the 3 models above for 20 epochs each

    Create these graphs:

    Graph 1: Test/Validation Loss for all 3 models together 
    Graph 2: Test/Validation Accuracy for 3 models together

This assignment has two scripts:

    1. EVA8_Assignment5_model
    2. EVA8_Assignment_main

**EVA8_Assignment5_model**

    This script defines a class for 3 normalization approaches- Layer/Group/Batch

**EVA8_Assignment_main**

    This script uses the network from Assignment 4 (Best model - Attempt2) and calls the normalization scrpit(EVA8_Assignment5_model)


**In a for loop network is run for all 3 normalization methods , 20 epochs each**

    Plot the accuracy of 3 normalization methods

    Plot the loss of 3 normalization methods

    Plot the mis classified images from 3 normalization methods
    
#**Normalization function**

    The below code defines three types of normalization Group, Batch and Layer normalization.

    The below are the links to the papers.

    Layer Normilzation : https://arxiv.org/pdf/1607.06450.pdf

    Group Normalization : https://arxiv.org/pdf/1803.08494.pdf

    Batch Normalization : https://arxiv.org/pdf/1502.03167.pdf

    This normalization function is called in the network (taken from assignment4 best model- attempt 2)

**Batch Normalization:**

    Introduced to tackle internal covariate shift. During training as the parameters are learnt from one layer optimised for that layer, while the input in the next layer are different. It causes the slowing down of the training process of a DNN due to slower convergence.

    BN allows to speed up the process by normalising the input to layers therby ensuring not too much shift in the distribution of inputs between layers leading to faster convergence

    The mean and standard deviation used for normalization are computed from the data set before the taining the network

    In BN the pixels sharing the same channel index are normalized together, ie for each channel, BN computes mean and standard dev.

**Group Normalization:**

    This approach takes the channels divides them into groups and then for each group computes the mean and variance that is used for normalization.

    The GN is independent of the batch size.

    GN the mean and standard dev are computed across channels in a given group

    The groups are obtainted by channel/G (G = 32 is the hyper parameter)

    if G=1 then GN becomes layer normalization

**Layer Normalization**

    Takes all channels in a current epoch

    Compute the Mean and Standard Dev across the channels

**Visualization**

Accuracy comparison across 3 normalization methods over 20 epochs

![Accuracy vs Epochs](https://github.com/rssubramaniyan1/EVA8/blob/main/Assignment%205/Accuracy%20vs%20Epochs.png)

Loss Comparison across 3 normalization methods over 20 epochs

![Loss vs Epochs](https://github.com/rssubramaniyan1/EVA8/blob/main/Assignment%205/Loss%20vs%20Epochs.png)

Mis classified Images(LN)

![LN_Misclassified_Images](https://github.com/rssubramaniyan1/EVA8/blob/main/Assignment%205/LN_Misclassified%20Images.png)

Mis classified Images(BN)

![BN_Misclassified_Images](https://github.com/rssubramaniyan1/EVA8/blob/main/Assignment%205/BN_Misclassified%20Images.png)

Mis classified Images(GN)

![GN_Misclassified_Images](https://github.com/rssubramaniyan1/EVA8/blob/main/Assignment%205/GN_Misclassified%20Images.png)


