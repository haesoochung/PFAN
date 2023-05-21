# PFAN

Official Tensorflow implementation of our paper: Pyramidal Feature Adjustment Networks for High Dynamic Range Imaging of Dynamic Scenes

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
3. Train
```
python main.py --mode train
```
## Test
```
python main.py --mode test 
```
