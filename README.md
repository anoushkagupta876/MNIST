# MNIST

## Standard Training
The architecture used is CNN. It starts with 2 Convulational layers that extract varying features from the input image, followed by a ReLu activation function to introduce non-linearity. There is a max pooling for each to decrease the dimensionality of the feature maps as well as to decrease the computational load and take care of overfitting by taking an abstracted form of features. And finally to make sense of these abstracted features we apply the fully connected layers to map them to 10 classes each representing the probability of that particular class or digit.

After 5 epochs, the observed test accuracy is Accuracy: 98.95%

#### Model Accuracy on Adversial Examples FGSM
<img width="350" alt="image" src="https://github.com/anoushkagupta876/MNIST/assets/63289179/68d23354-5740-48ef-a54b-40b8b90582d0">

## FGSM Trained Model
The model trained exclusively on FGSM adversarial images
#### Model Accuracy on Adversial Examples FGSM
<img width="400" alt="image" src="https://github.com/anoushkagupta876/MNIST/assets/63289179/7de78045-f2d6-47da-b1eb-4b0d065d4f17">

## PGD Trained Model
The model trained exclusively on PGD adversarial images
#### Model Accuracy on Adversial Examples FGSM
<img width="400" alt="image" src="https://github.com/anoushkagupta876/MNIST/assets/63289179/982f4319-0865-47c8-a537-563f552d2527">

#### Model Accuracy on Adversial Examples PGD
<img width="400" alt="image" src="https://github.com/anoushkagupta876/MNIST/assets/63289179/d630c2d5-eb6b-4ce6-8c58-f90d5f9944c4">

## Conclusion
This is for epsilon = 0.2

| Traing Model                         | Standard Training  | FGSM Training | PGD Training |
|--------------------------------------|--------------------|---------------|--------------|
| Standard Test Accuracy               | 0.9888             | 0.9556        | 0.9843       |
| Robust Test Accuracy (FGSM Attack)   | 0.8592             | 0.9805        | 0.9439       |
| Robust Test Accuracy (PGD Attack)    | 0.9120             | 0.9082        | 0.9815       |

 ### => PGD adversarial training significantly enhances model robustness, achieving high accuracy against both FGSM and PGD attacks, without compromising performance on clean data

