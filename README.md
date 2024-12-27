# ImageNet Training with ResNet

This project implements ResNet50 training on the ImageNet dataset using PyTorch. The implementation includes memory optimization, learning rate scheduling, and checkpoint management.

## Features

- ResNet50 architecture implementation
- Learning rate warmup and scheduling
- Gradient clipping for training stability
- Automatic checkpointing system
- Memory optimization for large-scale training
- TensorBoard integration for monitoring

## Requirements

- PyTorch 2.0
- Python 3.10
- CUDA 12.0
- cuDNN 8.9
- NVIDIA GPU

## Dataset

The ImageNet dataset used to test the model locally can be downloaded from:
- [ImageNet Mini](https://www.kaggle.com/datasets/ifigotin/imagenetmini-1000) (Subset of ImageNet with 1000 classes)

The ImageNet dataset used in this project can be downloaded from:
- [ImageNet Mini](https://www.kaggle.com/datasets/ifigotin/imagenetmini-1000) (Subset of ImageNet with 1000 classes)

Official link to ImageNet dataset:
- [ImageNet Official](https://www.image-net.org/download.php) (Full ImageNet dataset, requires registration)

## Dataset Setup

The ImageNet dataset should be organized as:

imagenet/
└── ILSVRC/
└── Data/
└── CLS-LOC/
├── train/
└── val/

## Training Monitoring

Monitor training progress using TensorBoard:
```
bash
tensorboard --logdir=runs
```

This will show:
- Training loss
- Test accuracy (Top-1 and Top-5)
- Learning rate changes
- Test loss


## Checkpoints

The model automatically saves:
- Regular checkpoints every 5 epochs
- Latest checkpoint after each epoch
- Emergency checkpoint if training is interrupted

Checkpoints are stored in the `checkpoints/` directory.

## Model Architecture

- ResNet50 with [3, 4, 6, 3] layer configuration
- Bottleneck blocks
- Batch normalization
- SGD optimizer with momentum
- Learning rate warmup and step decay

## License

[Choose an appropriate license]

## Acknowledgments

- ImageNet dataset
- PyTorch framework