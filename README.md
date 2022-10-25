# MIA
Code submission for Trustworthy Machine Learning Challenge 2022

The structure of this folder should be as following:
```
.
├── datasets
│   ├── eval
│   │   ├── cifar100_mobilenetv2.p
│   │   ├── cifar100_resnet34.p
│   │   ├── cifar100_vgg16.p
│   │   ├── cifar10_mobilenetv2.p
│   │   ├── cifar10_resnet34.p
│   │   ├── cifar10_vgg16.p
│   │   ├── tinyimagenet_mobilenetv2.p
│   │   ├── tinyimagenet_resnet34.p
│   │   └── tinyimagenet_vgg16.p
│   └── test
│       ├── cifar100_mobilenetv2.p
│       ├── cifar100_resnet34.p
│       ├── cifar100_vgg16.p
│       ├── cifar10_mobilenetv2.p
│       ├── cifar10_resnet34.p
│       ├── cifar10_vgg16.p
│       ├── tinyimagenet_mobilenetv2.p
│       ├── tinyimagenet_resnet34.p
│       └── tinyimagenet_vgg16.p
├── exp.ipynb
├── models
│   ├── mobilenetv2_cifar100.pth
│   ├── mobilenetv2_cifar10.pth
│   ├── mobilenetv2.py
│   ├── mobilenetv2_tinyimagenet.pth
│   ├── resnet34_cifar100.pth
│   ├── resnet34_cifar10.pth
│   ├── resnet34.py
│   ├── resnet34_tinyimagenet.pth
│   ├── vgg16_cifar100.pth
│   ├── vgg16_cifar10.pth
│   ├── vgg16_tinyimagenet.pth
│   └── vgg.py
├── README.md
├── result.json
└── results
    ├── task1_mobilenetv2_cifar100.npy
    ├── task1_mobilenetv2_cifar10.npy
    ├── task1_mobilenetv2_tinyimagenet.npy
    ├── task1_resnet34_cifar100.npy
    ├── task1_resnet34_cifar10.npy
    ├── task1_resnet34_tinyimagenet.npy
    ├── task1_vgg16_cifar100.npy
    ├── task1_vgg16_cifar10.npy
    ├── task1_vgg16_tinyimagenet.npy
    ├── task2_mobilenetv2_cifar100.npy
    ├── task2_mobilenetv2_cifar10.npy
    ├── task2_mobilenetv2_tinyimagenet.npy
    ├── task2_resnet34_cifar100.npy
    ├── task2_resnet34_cifar10.npy
    ├── task2_resnet34_tinyimagenet.npy
    ├── task2_vgg16_cifar100.npy
    ├── task2_vgg16_cifar10.npy
    ├── task2_vgg16_tinyimagenet.npy
    ├── task3_mobilenetv2_cifar100.npy
    ├── task3_mobilenetv2_cifar10.npy
    ├── task3_mobilenetv2_tinyimagenet.npy
    ├── task3_resnet34_cifar100.npy
    ├── task3_resnet34_cifar10.npy
    ├── task3_resnet34_tinyimagenet.npy
    ├── task3_vgg16_cifar100.npy
    ├── task3_vgg16_cifar10.npy
    └── task3_vgg16_tinyimagenet.npy
```

We use metric based appproaches for all three tasks. For task1 and task2, we use the confidence, entropy, modified entropy, and crossentropy loss as metrics to seperate member and non-member images, and evaluate the accuracy on the `eval` dataset. We plot the relationship between accuracy and threshold selction, and use the threshold with the highest accuracy to conduct the attack. For task3, we merely classify the member and non-member images by the prediction correctness.

## Usage
Clone this repository, download `participant.tar.gz` from `https://pan.baidu.com/s/1bAUQ-tcYR-gfjdyZSu-1tw?pwd=phi3` and extract it, copy `models` and `datasets` here, and then run `exp.ipynb`.

## Reference
[Membership Inference Attacks on Machine Learning: A Survey](https://arxiv.org/abs/2103.07853)