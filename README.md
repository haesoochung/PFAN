# PFAN

Official Tensorflow implementation of our paper: Pyramidal Feature Adjustment Networks for High Dynamic Range Imaging of Dynamic Scenes

## Overview
[framework.pdf](https://github.com/haesoochung/PFAN/files/11524958/framework.pdf)

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
3. Train
```
python main.py --mode train
```
## Test
```
python main.py --mode test 
```
