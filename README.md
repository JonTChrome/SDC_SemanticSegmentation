# Semantic Segmentation
### Goals
The goal of this project is to construct a Fully Convolutional Network complete with encoding and decoding sections as well as skip levels.  The network will be trained to label the pixels of road in given images

### Repo
The original project repository can be found [here](https://github.com/udacity/CarND-Semantic-Segmentation)

### Implementation

#### load_vgg
This function loaded the pre-trained encoder section of the network from the tensorflow module, the layer labels were given

#### layers
The using the layers from the previous function, this function constructed the layers needed for the FCN.  Skip layers were also added for spatial retention and the final layer was returned.

#### optimize
This function was needed to define the conditions under which the network would train itself

#### train_nn
Define the batch size and number of epoch and this function runs the training operations for the given parameters

#### run
The main entry point for the FCN to construct, train and validate on images.  This function calls the previous functions in succession to test the network and finishes by calling the helper function to validate the network on the test images.