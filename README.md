# CNN on MNIST using PyTorch

Using CNNs with data augmentation and regularization to achieve 99.2 % accuracy using less than < 13K parameters

## Model
 - ----------------------------------------------------------------
 -       Layer (type)               Output Shape         Param #
 - ================================================================
 -           Conv2d-1            [-1, 4, 26, 26]              36
       BatchNorm2d-2            [-1, 4, 26, 26]               8
              ReLU-3            [-1, 4, 26, 26]               0
            Conv2d-4            [-1, 8, 24, 24]             288
              ReLU-5            [-1, 8, 24, 24]               0
            Conv2d-6           [-1, 16, 22, 22]           1,152
       BatchNorm2d-7           [-1, 16, 22, 22]              32
         Dropout2d-8           [-1, 16, 22, 22]               0
              ReLU-9           [-1, 16, 22, 22]               0
        MaxPool2d-10           [-1, 16, 11, 11]               0
           Conv2d-11           [-1, 16, 11, 11]             256
             ReLU-12           [-1, 16, 11, 11]               0
           Conv2d-13             [-1, 32, 9, 9]           4,608
             ReLU-14             [-1, 32, 9, 9]               0
           Conv2d-15              [-1, 8, 7, 7]           2,304
      BatchNorm2d-16              [-1, 8, 7, 7]              16
        Dropout2d-17              [-1, 8, 7, 7]               0
             ReLU-18              [-1, 8, 7, 7]               0
           Conv2d-19             [-1, 10, 1, 1]           3,920
 ================================================================
  Total params: 12,620
  Trainable params: 12,620
  Non-trainable params: 0



## Observations
- Updated the Network to reduce the paramters and brought it to under 13K
- Added Batch Normalization, Dropout after the conv block
- Achieved accuracy of 99.2%
