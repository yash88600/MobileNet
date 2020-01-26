# MobileNet-from-scratch
Animal Classification using MobileNet from scratch

# MobileNet
* Used for mobile and embedded applications
* uses **Depthwise Separable Convolution(Depthwise Conv + Pointwise Conv)** instead of standard convolution 
    * Depthwise conv applies a single filter to each input channel, Pointwise conv then applies a 1x1 filter to combine the output of depthwise conv
* uses two parameters : **Width multiplier and Resolution Multiplier** to efficiently trade-off between latency and accuracy
    * The role of Width Multiplier is to thin a network at each layer (basically reduces the number of channels)
    * The role of Resolution Multiplier is to reduce the size of the layer
* these parameters allow user to choose the model architecture based on constraints and application
* The architecture has total **28 layers**(when counted Depthwise Conv & Pointwise Conv as two seperate layers)


![**Architecture**](https://github.com/yash88600/MobileNet-from-scratch/blob/master/mobilenet%20architecture.png)

