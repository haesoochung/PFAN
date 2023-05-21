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
