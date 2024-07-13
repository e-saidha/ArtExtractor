Task:
Develop a model using convolutional-recurrent architectures to classify artistic attributes such as Style, Artist, Genre, and more, both in general and specific contexts.

Requirements:
torch
torchvision
matplotlib
PIL
os
pandas
numpy

Model Architecture:
The model utilizes a pretrained ResNet-18, known for its superior performance and efficiency over building a model from scratch. The ResNet-18 is modified by removing the average pooling and fully connected layers to extract features. These features are then processed through an LSTM layer and a fully connected layer for final classification.

Actual Model:
The proposed model integrates multiple pretrained CNNs (AlexNet, GoogLeNet, VGGNet, and ResNet) to extract diverse features from various layers of entire images. These features are concatenated into a single tensor, reshaped for LSTM input, which processes the tensor representing the input information. The output sequence undergoes global average pooling, is flattened, and finally passed through a fully connected layer for classification.

Reference:
Dataset used: Wiki Art Dataset
Models referenced: ResNet (arXiv:1512.03385), RNN (arXiv:1308.0850)
Potential future upgrade: MDPI Sensor Journal

Note:
The original dataset size was 63 GB. Due to system constraints, a reduced version from Roboflow was used, which includes 15,274 images processed with specific augmentations and resizing.






