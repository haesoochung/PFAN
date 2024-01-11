# PFAN

This repository contains the official Tensorflow implementation of the following paper:

> **Pyramidal Feature Adjustment Networks for High Dynamic Range Imaging of Dynamic Scenes**<br>
> Haesoo Chung and Nam Ik Cho<br>
> https://ieeexplore.ieee.org/document/10171364
>
> **Abstract:** *Multi-exposure high dynamic range (HDR) imaging aims to generate an HDR image from multiple low dynamic range (LDR) images. There are two main challenges in this task; camera and object
motions causing ghost artifacts and over/under-exposure areas having no information. To tackle these challenges, we propose a deep neural network that aligns the multiple inputs through feature transformation
and hallucinates the washed-out areas after fusion. Specifically, we propose a pyramidal feature adjustment network (PFAN) that adjusts the reference image features’ brightness and structure with respect to LDR
inputs and regard them as the aligned features of the LDR inputs. Then, the features from the PFANs are integrated in a coarse-to-fine manner. They are first merged into an HDR image in a fusion network, and
the washed-out regions are restored using valid information in a hallucination network. To deal with larger displacements in motion alignment, we also present a progressive training strategy, which begins the training
with easy samples having little motion and then transfers the network with more dynamic samples. Extensive experiments demonstrate that our method achieves state-of-the-art performance on benchmark datasets.*

## Overview
![framework](https://github.com/haesoochung/PFAN/assets/92298918/9a4763ae-32cc-4dca-988c-487b6ee19cc8)

## Dependencies
* Python
* Tesorflow 
* OpenCV

## Training
1. Download Kalantari dataset from https://cseweb.ucsd.edu/~viscomp/projects/SIG17HDR/.
2. Make tfrecords
```
python utils/make_tfrecords.py
```
3. Download the [pre-trained vgg16 model](https://drive.google.com/file/d/1-Pp-ZBzrGxgIh5VlyBWZcRly8QT5ZhnG/view?usp=sharing) in the "utils" folder.
4. Train
```
python main.py --mode train
```
## Test
1. Make a folder named checkpoints and download the [pre-trained model weight](https://drive.google.com/drive/folders/1g_aOOHLm204uQPz4pVj1WbD8Fg47bcrc?usp=share_link).
```
mkdir checkpoints
cd checkpoints
```
2. Test
```
python main.py --mode test 
```

## Results
![fig5](https://github.com/haesoochung/PFAN/assets/92298918/7367d018-7971-43dc-a9a0-424c3669c563)
![fig6](https://github.com/haesoochung/PFAN/assets/92298918/45fbd469-cf70-44ce-8814-6b7b403cc568)
![fig7](https://github.com/haesoochung/PFAN/assets/92298918/b577ad36-a68c-4f5e-a230-bf7172215d06)
![fig8](https://github.com/haesoochung/PFAN/assets/92298918/5d831f9d-4536-48fa-8f25-8f3c9b0094a8)
![supple1](https://github.com/haesoochung/PFAN/assets/92298918/25e0079b-cdf4-4ad0-ac87-905af6c6ddef)
![supple2](https://github.com/haesoochung/PFAN/assets/92298918/5a65e48a-3285-42c3-ad02-4e04c420de5d)
![supple3](https://github.com/haesoochung/PFAN/assets/92298918/19ec70b5-3923-4799-b3d6-ed13c701c6ef)

## Citation
```
@article{chung2023pyramidal,
  title={Pyramidal Feature Adjustment Networks for High Dynamic Range Imaging of Dynamic Scenes},
  author={Chung, Haesoo and Cho, Nam Ik},
  journal={IEEE Access},
  year={2023},
  publisher={IEEE}
}
```
