# Project3-Self-Driving-Car-Image-Segmentation
![selfDriving](https://github.com/user-attachments/assets/1290bead-d546-4a45-8e33-23cfe36f4dcf)

## Introduction:
Major cities worldwide are facing two major problems on the streets: congestion and a high number of traffic accidents. According to the WHO, road traffic is one of the most complex and dangerous systems we face daily. One of the main factors that cause traffic accidents is driver negligence.

Self-Driving Car technology equipped with Artificial Intelligence (AI) has great potential to reduce accidents and congestion. With AI's ability to segment objects in images from the vehicle's perspective, this system can assist in faster and more accurate decision-making on the road, thereby reducing the likelihood of accidents caused by human error.

## Objective: 
This project aims to build an AI system capable of segmenting objects from images and videos that are expected to identify important objects on the road, such as other vehicles, pedestrians, and traffic signs, under various weather and lighting conditions. We will implement three popular segmentation algorithms: FCN8, U-Net, and SegNet. The project will include implementation, optimization (hyperparameter tuning), and evaluation to determine the most effective algorithm.

## Features:
- `Dataset`: Using the Cityscapes dataset, which contains images of urban environments from the perspective of a car with annotations for various objects such as roads, vehicles, pedestrians, and more.
- `Deep Learning Model`: Implements three popular segmentation models:
   1. **FCN8 (Fully Convolutional Network)**: This model uses full convolution without dense layers, which enables high-resolution image segmentation. FCN8 combines information from different resolution levels to produce more accurate segmentation.
   2. **U-Net**: This model is known for its "U" shaped architecture that consists of a contractive path to capture context and an expansive path to enable high-precision segmentation. U-Net is particularly effective for image segmentation where object edge details are critical.
   3. **SegNet**: This model adopts a symmetric encoder-decoder, where the encoder reduces the input resolution to extract important features, while the decoder restores the resolution to produce object segmentation. SegNet excels in memory efficiency and processing speed.

  Those three models were tested with three different CNN architectures as base models:
    1. **Vanilla CNN**: The basic CNN architecture for performance baseline, consisting of simple convolution and pooling layers.
    2. **VGG-16**: A CNN architecture with a depth of 16 layers, known for its ability to capture complex visual features.
    3. **ResNet-50**: CNN architecture that uses residual blocks to overcome performance degradation issues in very deep networks, with 50 layers.
