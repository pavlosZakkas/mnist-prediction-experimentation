# Experimentation with mnist and fashion-mnist datasets

A sequence of experiments were performed for the mnist and fashion-mnist datasets, including Convolutional Neural Networks (CNN) and Multi-Layer Perceptron (MLP) networks. 

Tensorboard was integrated in order to store and present the results.

## CNN 
The performance of different CNNs was investigated, in which the following parameters were tested:
- different **convolutional layers**, with various filters, kernel sizes, pooling layers and dropouts
- different **dense layers**, with different sizes of neurons
- **optimizer**: Momentum, Nesterov, RMSProp, Adagrad, Adam, Adadelta
- **activation**: sigmoid, ReLU, LeakyReLU, ELU, SELU
- **weights initialization**: HE normal for sigmoid, ReLU and variants, except fot SELU where Lecun normal was used

## MLP
A variety of MLP networks was also invetsigated in which the following parameters were tested:
- different **dense layers**, with different sizes of neurons
- **regularization**: l1, l2, l1_l2, dropout with various dropout rates
- **optimizer**: Momentum, Nesterov, RMSProp, Adagrad, Adam, Adadelta
- **activation**: sigmoid, ReLU, LeakyReLU, ELU, SELU
- **weights initialization**: HE normal for sigmoid, ReLU and variants, except fot SELU where Lecun normal was used

## Permutation of pixels
The impact changing the input images by permuting their pixels is also demonstrated. As expected, the change has no impact on MLP network, whereas CNN's performance decreases since they cannot extract the same spatial information of the images as before permutation.