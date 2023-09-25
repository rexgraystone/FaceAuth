# FaceAuth

FaceAuth is a repository housing a state-of-the-art Generative Adversarial Network (GAN) designed to distinguish between real human faces and artificially generated ones.
The dataset utilized for training has been customized from a [Kaggle dataset](https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces).

## Methodology

The model was trained for 15 epochs, with early stopping in kicking in at 5, with a batch size of 32. The model was trained on RTX 3080 Ti.

## Model Architecture

The model uses a base layer of ResNet50.

<p align='center'>
    <img src="Images/FaceAuth_architecture.png" alt='FaceAuth Model Architecture'>
</p>

### ResNet50



## Results

The model trained on the raw images achieved an accuracy of 84.35%, while the model trained on the masked images achieved an accuracy of 90.13%. This is a good improvement over the raw images. The accuracy can be further improved by training the model for more epochs, and by using a larger dataset.

Accuracy Plot

<p align='center'>
    <img src="Images/FaceAuth_accuracy.png" alt='Accuracy Plot' width="75%" height="75%">
</p>

Loss Plot

<p align='center'>
    <img src="Images/FaceAuth_loss.png" alt='Loss Plot' width="75%" height="75%">
</p>
