# Ensemble-Based Out-of-Distribution Detection

## Introduction
This project is for the paper "Ensemble-Based Out-of-Distribution Detection" in MDPI Electronics. Some codes are from [ODIN](https://github.com/facebookresearch/odin) and [Mahalanobis-based OOD Detection](https://github.com/pokaxpoka/deep_Mahalanobis_detector/).

## Requirements
- Python 3.7
- Pytorch 1.5 (GPU version is recomended)
- scipy
- scikit-learn
- numpy
- ETC.

## Experiments
We provide several expeiments of ood detection using various combinations of datasets. 
- 1-Channel image datasets: MNIST, and FashionMNIST
- 3-Channel image datasets: CIFAR-10, CIFAR-100, SVHN, Tiny ImageNet, and LSUN,

## Downloading Datasets
The datasets, excluding Tiny ImageNet and LSUN, are automatically downloaded from our code using the PyTorch library.
To download Tiny ImageNet and LSUN datasets, we use following links from [ODIN](https://github.com/facebookresearch/odin).
- [Tiny ImageNet](https://www.dropbox.com/s/kp3my3412u5k9rl/Imagenet_resize.tar.gz)
- [LSUN](https://www.dropbox.com/s/moqh2wh8696c3yl/LSUN_resize.tar.gz)

Please download and place them to `./data/`.

## Training Models (ResNet34, Siamise with ResNet34, Triplet with ResNet34)
The models, excluding ResNet34 on 3-Channel image, are trained in our code(network_trainer_1C.ipynb, and network_trainer_3C.ipynb)
To download the trained ResNet34 on 3-Channel image, we provide following links.
- Trained Model Weights: [ResNet on CIFAR-10](https://drive.google.com/file/d/1RWaAn4AKdc7pvdrDgtjCX20pkKFcUZLG/view), [ResNet on CIFAR-100](https://drive.google.com/file/d/1dD3M5dl8uCqCV1W3z1_Jjh82XaKgtyYT/view), [ResNet on SVHN](https://drive.google.com/file/d/1-8UvIYaYxmpfbZjA2hCiroOObCmP50ce/view)
- Trained Model: [ResNet on CIFAR-10](https://drive.google.com/file/d/1GOKXr7h4sX7Yh7jX7hdOZeDUXh0L-oLo/view), [ResNet on CIFAR-100](https://drive.google.com/file/d/1Jv3PstIGQzRoC_5zJTIPCopaovla_bWP/view), [ResNet on SVHN](https://drive.google.com/file/d/1DHibbI_-5aVcsXYO2W1L7KLrbD9Daky8/view)

Please download and place them to `./trained_models/`.

- Run all code in network_trainer_1C.ipynb, and network_trainer_3C.ipynb.
- You can see all trained models in `./trained_models/`.

### Out-of-distribution Detection (Baseline Method, ODIN, Mahalanobis-based Method, DML-based Method (ours) )
- Run all code in MAIN_1c.ipynb and MAIN_3c.ipynb
- All results will be printed in the each cell of Main_1c and Main_3c notebook  
