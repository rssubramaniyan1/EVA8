#**Import the data module**

     The data module downloads the CIFAR 10 dataset and applies the respective train and test transformation on the data.

    The data has 50k train samples and 10k test with a total of 10 classes

    The data module also calls the utils which has the functions for transformation defined

#**Import the utils module**
    function to calculate mean and standard deviation of the dataset

    function to apply transformations on the train dataset

    function to apply transformations on the test dataset

    function for the optimizer and schedule

    function for training and testing the model

#**Import the network (model architechture)**
    The model has depthwise separable convolution

    Has less than 50k parameters

    Tried various combinations of max pool and dilated cov

    **Error always at 2.30 / Accuracy = 10% consistently across different architechtures. This needs fixing.**
    
 !["Network Summary"](https://github.com/rssubramaniyan1/EVA8/blob/d245d9836ba67122051f7f43686906e30821466f/Assignment%206/Network%20Summary.png)
 
 ![ Test_Train_Accuracy](https://github.com/rssubramaniyan1/EVA8/blob/d245d9836ba67122051f7f43686906e30821466f/Assignment%206/Test_Train_Accuracy.png)
 
 

