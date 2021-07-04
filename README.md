# VINS_Lite_GPU
VINS FUSION GPU lite version. 

## What we have done

- Memory leak problem is fixed. 
- We trained a DBOW vocabulary with LIP6Indoor dataset. This model can achieve 95% of the performance of the original model.
- We have test this model on Nvidia Jetson Nano 2GB version. The RAM consumption is 60MB when program starts up. The usage of RAM will increase with the number of keyframe or running time. The GPU consumption is about 20%.  

![vins_lite_gpu-2](https://user-images.githubusercontent.com/17807222/124372174-6c5d9700-dcbb-11eb-8bec-cb5755701528.png)

## Installation
Please follow original [VINS FUSION GPU](https://github.com/pjrambo/VINS-Fusion-gpu). The installation process is identical.


