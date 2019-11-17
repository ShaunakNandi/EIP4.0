# Assignment 1

# Convolutions

The basic operation of learning the features of an image. Convolution includes an element wise multiplication, calculated to identify edges and gradients of the input image from the previous layer.

# Filters/ Kernels

The window operation which implements the element wise multiplication. It is a weighing function which helps retain important information
while removing noise/ unimportant features by multiplying such pixel value by small factors. Kernels can help identify colors, edges or 
gradients. 

Ideally kernels are 3x3 windows. These values may be randomly initialised and are updated every iteration via the back-prop to increase the
accuracy of the model. Ultimately, this process updates the weight matrix.

![kernels](https://i.stack.imgur.com/5yGWY.png "kernels")

# Epochs

An iteration where the model computes convolution over every image of the input train dataset once, is called epoch. The number of epochs when training the model must be defined carefully to prevent models from halucinating (over/ under fitting). 

# 1x1 convolutions

These are typically used to reduce the number of channels without losing out on the important features detected by the model on training. Output of 1x1 convolutions retain the maximising features and merges them into preset number of output channels. Overall, density of calculations is thus reduced.

# 3x3 convolutions:

1. They are heavily optimised (hardware accelerated in the libraries)

2. Odd indexed kernels are essential to maintain the symmetry about the central pixel. Else there may arise:
    1. Distortion (uneven convolutions across the entire image)
    2. Loss of information over multiple stages (round off to lower image resolution)
    
3. They help build lighter models:
    1. Executing 3x3 twice is equivalent to a single 5x5 convolution. However, 
         1. 3x3 twice: (3 * 3) * 2 = 18 parameters
         2. 5x5 once:  (5 * 5) * 1 = 25 parameters
         
         Hence 3x3 is extremely favourable
         
    2. This can be furthur exploited by using spatially seperable convolutions
    
# Feature Maps
 
The output of the feature extractors/ filters/ kernels. It can be colors or edges. The number of maps generated at output of each convolution layers is independent of the number of input channels but is typically 32x (GPU core optimised)

# Activation Functions

It is almost an impurity defined into the network to introduce non-linearity. It is aimed at making the model more robust and detect objects presented from an unusual angle/ orientation.

# Receptive Field

It is the number of pixels each convolution filter 'sees'. It is how the model learns if the feature is an edge (locally) but also if it is a arc or circle etc (global). Finally the model can learn to identify the object overall as well as the scenery around it.

edges and gradients -> textures -> patterns -> parts of objects -> objects -> scenes

- - - -

Please click this [link](https://colab.research.google.com/drive/13yneZmMb7Wd80iV3oLfB83cDahOzWXe6) if the notebook does not render.
