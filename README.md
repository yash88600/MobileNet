# MobileNet-from-scratch
Animal Classification using MobileNet from scratch

# MobileNet
* Used for mobile and embedded applications
* uses **Depthwise Separable Convolution(Depthwise Conv + Pointwise Conv)** instead of standard convolution 
    * Depthwise conv applies a single filter to each input channel, Pointwise conv then applies a 1x1 filter to combine the output of depthwise conv
* uses two parameters : **Width Multiplier and Resolution Multiplier** to efficiently trade-off between latency and accuracy
    * The role of Width Multiplier is to thin a network at each layer (basically reduces the number of channels)
    * The role of Resolution Multiplier is to reduce the size of the layer
* these parameters allow user to choose the model architecture based on constraints and application
* The architecture has total **28 layers**(when counted Depthwise Conv & Pointwise Conv as two seperate layers)

# Architecture
![**Architecture**](https://github.com/yash88600/MobileNet-from-scratch/blob/master/mobilenet%20architecture.png)

# Computational Cost:
![**Cost**](https://github.com/yash88600/MobileNet-from-scratch/blob/master/mobilenetcomputation%20cost.PNG)

# Application:
* **Used MobileNet for Animal Classification(10 classes)**
* Architecture: MobileNet with Width multiplier=1 & Resolution Multiplier=0.57
* Dataset: Animals-10 provided by Corrado Alessio on Kaggle: https://www.kaggle.com/alessiocorrado99/animals10
     * Input size: 128x128x3
     * Output: 10 classes
     * No of training samples: 26,180
* Optimizer: RMSprop with learning rate=0.002
* Loss function: categorical_crossentropy
* Batch Size: 128
* No of Epochs: 50
* **The best result was obtained on 42th epoch with**
     * **Training accuracy: 98.45%**
     * **Validation acuracy: 75.55%**
 We present a class of efficient models called MobileNets for mobile and embedded vision applications. MobileNets are based on a streamlined architecture that uses depth-wise separable convolutions to build light weight deep neural networks. We introduce two simple global hyper-parameters that efficiently trade off between latency and accuracy. These hyper-parameters allow the model builder to choose the right sized model for their application based on the constraints of the problem. We present extensive experiments on resource and accuracy tradeoffs and show strong performance compared to other popular models on ImageNet classification. We then demonstrate the effectiveness of MobileNets across a wide range of applications and use cases including object detection, finegrain classification, face attributes and large scale geo-localization.
      
 **For more information about MobileNet,Refer to the original paper:** https://arxiv.org/abs/1704.04861
