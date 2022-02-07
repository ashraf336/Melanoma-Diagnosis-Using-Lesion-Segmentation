# Melanoma-Diagnosis-Using-Lesion-Segmentation

Contributors:

Ahmed Ashraf 

Abdulrahman HAbib

Mohamed Aiman

Osama Sherif

Image segmentation is the task of assigning each pixel a label which is a class that it belongs
to. In binary segmentation, you only have two classes: foreground and background. In this
assignment we will work on a binary segmentation problem and we will implement and test
two famous architectures Fully Convolution Network and U-Net.

1.1 Melanoma Diagnosis Using Lesion Segmentation
In this task you will work on ISIC challenge where you will segment lesions (foreground) out
of dermoscopic images.
You will be using using ISIC’s 2017 train, validation and test sets. The train set consists
of 2000 images along with their ground truth masks and superpixel images(discard for this
assignment). The mask should contain 2 values: 0 for background and 255 for foreground.
During training you will convert the mask to 0, and 1 values before feeding it to the network.

1.2 Networks

1. Fully Convolution Network (FCN): It is implemented using a VGG-16 backbone but
instead of the 3 fully connected classification layers, the first two are replaced with a
1x1 convolution with the same number of filters. The last layer is replaced with 1x1
convolution layer with the number of filters equals the number of classes. Finally a
deconvolutional layer that upsamples the output to the original image size is added to
produce the final prediction.

2. UNet: Instead of producing the output as a sever upsampling out of the last feature map,
it designs a decoder that doubles the feature map size until it reaches the image size.
Also it introduces the skip connection technique to combine the encoder and decoder
learned features to produce finer segmentation masks. Refer to Figure 1 in the paper to
implement the network arcitecture.
