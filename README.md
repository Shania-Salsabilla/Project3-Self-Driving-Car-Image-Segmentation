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
   2. **U-Net**: This model is known for its _U_ shaped architecture that consists of a contractive path to capture context and an expansive path to enable high-precision segmentation. U-Net is particularly effective for image segmentation where object edge details are critical.
   3. **SegNet**: This model adopts a symmetric encoder-decoder, where the encoder reduces the input resolution to extract important features, while the decoder restores the resolution to produce object segmentation. SegNet excels in memory efficiency and processing speed.

  Those three models were tested with three different CNN architectures as base models:
    1. **Vanilla CNN**: The basic CNN architecture for performance baseline, consisting of simple convolution and pooling layers.
    2. **VGG-16**: A CNN architecture with a depth of 16 layers, known for its ability to capture complex visual features.
    3. **ResNet-50**: CNN architecture that uses residual blocks to overcome performance degradation issues in very deep networks, with 50 layers.
- `Model Training`: Each deep learning algorithm will be trained using the Cityscapes dataset that has been preprocessed with several scenarios:
   1. The FCN8 model is trained with Vanilla CNN, VGG-16, and ResNet-50 as base models.
   2. The U-Net model is trained with Vanilla CNN, VGG-16, and ResNet-50 as base models.
   3. The SegNet model is trained with Vanilla CNN, VGG-16, and ResNet-50 as base models.

## Folder Structure:
- `Dataset Project 3 Self Driving Car`:
   1. **annotations_prepped_test**: Folder containing annotations of prepped test data.
   2. **annotations_prepped_train**: Folder containing the annotations of the prepped training data.
   3. **images_prepped_test**: Folder containing the prepped test images.
   4. **images_prepped_train**: The folder containing the prepped training images.
- `Notebook Test on 9 Models`:
   1. **FCN8 Segmentation Model**: Notebook containing FCN8 segmentation model tests with Vanilla CNN, VGG-16, and ResNet-50 as base models.
   2. **Segmentation Model SegNet**: Notebook containing the SegNet segmentation model experiments with Vanilla CNN, VGG-16, and ResNet-50 base models.
   3. **U-Net Segmentation Model**: Notebook containing the experiments of U-Net segmentation model with Vanilla CNN, VGG-16, and ResNet-50 as base models.
- `Notebook Resnet50-Unet Finetuning`: There are four variations of notebooks resulting from fine-tuning the ResNet50-Unet model, focused on achieving the smallest validation dice loss value.
- `Gradio Inference on Google Colab`: A notebook containing an implementation of segmentation model inference using Gradio on Google Colab, allowing users to test models interactively.
- `Project 3-Self Driving Car.pdf`: A PDF presentation of the project that describes the entire project, experimental results, and conclusions.

## Links:
For support this project, here are some important links:
1. [Project 3: Object Segmentation Timeline & Results](https://docs.google.com/spreadsheets/d/19r60rSKzbD9wwQJAUAhbfaILK345ghxz2j73iuzR9q8/edit?usp=sharing): This link leads to a spreadsheet document that records the project timeline and comparison results of the various object segmentation models used in this project.
2. [Hugging Face Interface](https://huggingface.co/spaces/eurekalabdawara/computervision-keras-segmentation): This link goes to a demo of the application implemented with Gradio for segmentation model inference in Google Colab. It provides an interactive interface to test and assess the segmentation models developed during the project.
