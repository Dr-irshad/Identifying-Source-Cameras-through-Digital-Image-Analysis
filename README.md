# Investigating the Potential of Artificial Intelligence and Data Science Techniques in Identifying Source Cameras through Digital Image Analysis

## Project Overview
In the project **“Investigating the Potential of Artificial Intelligence and Data Science Techniques in Identifying Source Cameras through Digital Image Analysis,”** the main focus was to explore how emerging AI and data science techniques could aid in identifying the original source camera of digital images. The rise of image editing tools, tampering methods, and sophisticated signal processing technologies has made it increasingly difficult to ascertain the authenticity of digital images. This challenge has become more critical with the prevalence of digital data collection and image manipulation techniques, necessitating more effective methods to identify and authenticate source cameras. 

The project explored the concept of **PRNU (Photo Response Nonuniformity)**, a unique characteristic embedded in digital imaging sensors. The objective was to create a reliable and efficient model to address the challenge of identifying the original camera source, even when the image has undergone tampering using seam carving techniques that manipulate and obscure the camera’s identity. 

The primary solution proposed in the project was **IMGCAT**, an innovative AI model integrating 1D CNN (Convolutional Neural Network) for feature extraction on 20x20-pixel blocks. IMGCAT was designed to perform well in a three-class classification scenario, demonstrating state-of-the-art performance while maintaining robustness against various forms of image manipulations, particularly seam insertions and removals.

## Key Features and Highlights
- **PRNU (Photo Response Nonuniformity)** used for identifying the source camera.
- **Seam Carving Techniques**: Investigation of how common image tampering methods, such as seam carving, affect source camera identification.
- **IMGCAT Model**: Integration of a 1D CNN architecture for feature extraction and classification.
- **Three-Class Classification**: A classification system that distinguishes between different source cameras based on the image’s inherent characteristics.
- **Robustness**: The model demonstrated resilience against various types of image manipulations like seam insertions and removals.
- **State-of-the-Art Performance**: IMGCAT model outperformed previous methods in its ability to identify source cameras, even in tampered images.

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Methodology](#methodology)
4. [Model Architecture](#model-architecture)
5. [Results](#results)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Conclusions](#conclusions)
9. [License](#license)
10. [Acknowledgements](#acknowledgements)

## Introduction
With the increasing use of digital imaging devices, the authenticity of digital images has become a major concern. Image manipulation techniques, such as resizing, cropping, and seam carving, have made it easier to alter images while maintaining a natural appearance. As a result, identifying the source camera of an image is crucial for verifying its authenticity. The Photo Response Nonuniformity (PRNU) pattern embedded in digital sensors provides a unique identifier for each camera sensor, and this project aimed to use AI techniques to better detect and authenticate the source of images, even after they have undergone significant tampering.

## Objectives
The main objectives of this project were:
- To investigate the use of AI and data science techniques in identifying the source camera of digital images.
- To explore how sophisticated image manipulations, particularly seam carving, affect the ability to identify the source camera.
- To introduce a robust model for source camera identification, capable of handling tampered images.

## Methodology
The research was conducted using the following steps:
1. **Data Collection**: A dataset of digital images was compiled, focusing on images captured by different camera models.
2. **Preprocessing**: Images were preprocessed to extract features, focusing on the PRNU patterns in the images.
3. **Model Development**: The IMGCAT model was developed by integrating a 1D CNN for feature extraction. A sliding window approach was employed, extracting 20x20-pixel blocks to feed into the model.
4. **Classification**: The model was trained to classify the images into three distinct classes, each corresponding to a different source camera.
5. **Testing with Manipulations**: The model was tested with images that had undergone seam carving techniques (both insertions and removals), to assess its robustness against tampering.
6. **Evaluation**: Performance was evaluated using accuracy, precision, recall, and F1-score metrics.

## Model Architecture
The IMGCAT model integrates a **1D Convolutional Neural Network (CNN)** that operates on small image blocks (20x20 pixels). This feature extraction process helps capture fine-grained details in the images that are unique to each camera sensor, especially the PRNU pattern. The model architecture consists of:
- **Input Layer**: 20x20-pixel image blocks are fed into the model.
- **Convolutional Layers**: These layers extract key features from the input blocks.
- **Fully Connected Layers**: These layers process the extracted features to classify the images into three categories.
- **Output Layer**: The final output is a three-class prediction representing different source cameras.

## Results
The IMGCAT model demonstrated remarkable performance in identifying the source camera of digital images, even under manipulation. It showed:
- High accuracy in classifying images from different cameras.
- Robustness against image tampering, especially when using seam carving techniques.
- Improved performance compared to traditional image authentication methods.

## Installation
To install the project, follow the instructions below:

1. Clone the repository:
   ```bash
   git clone https://github.com/Dr-irshad/Identifying-Source-Cameras-through-Digital-Image-Analysis.git

2. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt
3. Ensure that you have TensorFlow or PyTorch installed, depending on the version used for training the CNN model.
4. Prepare the dataset and place it in the data/ directory.

## Usage
Once the project is set up, you can run the model with the following command:
    ```bash
    python src/run_model.py --image.jpg
This will predict the source camera for the given image. You can test the robustness of the model by providing images that have undergone various manipulations like seam carving.

## Conclusions
This project demonstrated the effectiveness of AI and data science techniques in identifying source cameras through digital image analysis. The use of PRNU patterns and the innovative IMGCAT model provided a promising solution to the problem of source camera identification. The model’s robustness against seam carving techniques highlights its potential as a reliable tool for image authentication in an era of digital manipulation.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
We would like to thank the researchers and developers whose work has contributed to the development of image forensics techniques, including those in the areas of PRNU extraction and image manipulation detection. Special thanks to the open-source community for providing valuable libraries and tools for AI and image processing.




