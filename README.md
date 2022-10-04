# Multiclass_Unet_tensorflow

U-Net is a convolutional neural network that was developed for biomedical image segmentation at the Computer Science Department of the University of Freiburg. The network is based on the fully convolutional network and its architecture was modified and extended to work with fewer training images and to yield more precise segmentations. 

The U-Net architecture stems from the so-called “fully convolutional network” first proposed by Long, Shelhamer, and Darrell.The main idea is to supplement a usual contracting network by successive layers, where pooling operations are replaced by upsampling operators. Hence these layers increase the resolution of the output. A successive convolutional layer can then learn to assemble a precise output based on this information.One important modification in U-Net is that there are a large number of feature channels in the upsampling part, which allow the network to propagate context information to higher resolution layers. As a consequence, the expansive path is more or less symmetric to the contracting part, and yields a u-shaped architecture. The network only uses the valid part of each convolution without any fully connected layers. To predict the pixels in the border region of the image, the missing context is extrapolated by mirroring the input image. This tiling strategy is important to apply the network to large images, since otherwise the resolution would be limited by the GPU memory.

The network consists of a contracting path and an expansive path, which gives it the u-shaped architecture. The contracting path is a typical convolutional network that consists of repeated application of convolutions, each followed by a rectified linear unit (ReLU) and a max pooling operation. During the contraction, the spatial information is reduced while feature information is increased. The expansive pathway combines the feature and spatial information through a sequence of up-convolutions and concatenations with high-resolution features from the contracting path.

There are many applications of U-Net in biomedical image segmentation, such as brain image segmentation (''BRATS''[4]) and liver image segmentation ("siliver07"[5]) as well as protein binding site prediction.[6] Variations of the U-Net have also been applied for medical image reconstruction.[7] Here are some variants and applications of U-Net as follows:
Pixel-wise regression using U-Net and its application on pansharpening;
3D U-Net: Learning Dense Volumetric Segmentation from Sparse Annotation;
TernausNet: U-Net with VGG11 Encoder Pre-Trained on ImageNet for Image Segmentation.
Image-to-image translation to estimate fluorescent stains
In binding site prediction of protein structure.
