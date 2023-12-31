# FaceAuth

FaceAuth is a repository housing a state-of-the-art deep learning model designed to distinguish between real human faces and artificially generated ones.

## Methodology

The model was trained for 15 epochs, with early stopping in kicking in at 5, with a batch size of 32. The model was trained on RTX 3080 Ti Laptop GPU.

## Installation

To install the required packages, run the following command in your terminal:

```bash
pip install -r requirements.txt
```

## Dataset

The dataset consists of 140,000 images of real human faces and artificially generated ones. The dataset was split into training, validation, and testing sets with 100k, 20k and 20k respectively. The dataset can be downloaded from [here](https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces).

<table align='center'>
  <tr>
    <td align="center">
      <img src="Images/sample_real.jpg" alt="Real image sample"/>
      <p>Figure 1: A real image sample</p>
    </td>
    <td align="center">
      <img src="Images/sample_fake.jpg" alt="Fake image sample"/>
      <p>Figure 2: A fake image sample</p>
    </td>
  </tr>
</table>

## Model Architecture

The model uses a base layer of ResNet50.

<p align='center'>
    <img src="Images/FaceAuth_architecture.png" alt='FaceAuth Model Architecture' width="20%" height="20%">
    <br>
    <p align='center'>Figure 3: FaceAuth Model Architecture</p>
</p>

### ResNet-50

Residual Networks, or ResNets, learn residual functions with reference to the layer inputs, instead of learning unreferenced functions. Instead of hoping each few stacked layers directly fit a desired underlying mapping, residual nets let these layers fit a residual mapping. They stack residual blocks ontop of each other to form network.
ResNet-50, short for "Residual Network 50," is a deep convolutional neural network architecture that belongs to the ResNet family. ResNet-50 is specifically known for its depth, consisting of 50 layers, making it a relatively deep neural network. For more information, refer to the [original paper](https://arxiv.org/abs/1512.03385).

## Results

FaceAuth achieved a training accuracy of 86.56%, training loss of 21.29%, validation accuracy of 92.33%, validation loss of 21.30%, testing accuracy of 91.69%, and testing loss of 23.26%. The accuracy can be further improved by training the model for more epochs and modifying the model architecture.

<table>
  <tr>
    <td align="center">
      <img src="Images/FaceAuth_accuracy.png" alt="FaceAuth Accuracy Plot"/>
      <p>Figure 4: FaceAuth Accuracy Plot</p>
    </td>
    <td align="center">
      <img src="Images/FaceAuth_loss.png" alt="FaceAuth Loss Plot"/>
      <p>Figure 5: FaceAuth Loss Plot</p>
    </td>
  </tr>
</table>
