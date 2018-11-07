# CapProNet 
We built our CapProNet with Resnet backbone from official tensorflow implementation.
# ResNet in TensorFlow
Deep residual networks, or ResNets for short, provided the breakthrough idea of identity mappings in order to enable training of very deep convolutional neural networks. This folder contains an implementation of ResNet for the ImageNet dataset written in TensorFlow.

See the following papers for more background:

[1] [Deep Residual Learning for Image Recognition](https://arxiv.org/pdf/1512.03385.pdf) by Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun, Dec 2015.

[2] [Identity Mappings in Deep Residual Networks](https://arxiv.org/pdf/1603.05027.pdf) by Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun, Jul 2016.

In code v1 refers to the resnet defined in [1], while v2 correspondingly refers to [2]. The principle difference between the two versions is that v1 applies batch normalization and activation after convolution, while v2 applies batch normalization, then activation, and finally convolution. A schematic comparison is presented in Figure 1 (left) of [2].

Please proceed according to which dataset you would like to train/evaluate on:


## CIFAR-100

### Setup

We used Tensorflow 1.6 and Python 2.7 to run our experiments.
First make sure you've [added the models folder to your Python path](/official/#running-the-models); otherwise you may encounter an error like `ImportError: No module named official.resnet`.

Then download and extract the CIFAR-100 data from Alex's website.

Then to train the model, run the following:

```
python Cifar100_main_lambda_inv_110l.py --data_dir= path/to/Cifar100
```

Use `--data_dir` to specify the location of the CIFAR-100 data used in the previous step. There are more flag options as described in `Cifar100_main_lambda_inv_110l.py`.


