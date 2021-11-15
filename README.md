# VINS_Lite_GPU

VINS FUSION GPU lite version. 

--- 

## Our works

- Memory leak problem is fixed. 
- We trained a DBOW vocabulary with LIP6Indoor dataset. This model achieves 95% of the performance of the original model, and much smaller.
- We have test this model on Nvidia Jetson Nano 2GB version with MYNTEYE s1030-ir. The RAM consumption is about 60MB when program starts up. The usage of RAM will increase with the number of keyframe or running time. The GPU consumption is about 20%.  

![vins_lite_gpu-2](https://user-images.githubusercontent.com/17807222/124372174-6c5d9700-dcbb-11eb-8bec-cb5755701528.png)

---

## Performance
It can be very easy to reach 30fps on Jetson Nano 2GB with half feature number cut down. Please check the pose_graph in RVIZ rather than tracking image view. The pose_graph is realtime, but the tracking image view has a serious delay. Here is my configuration:
```yaml
multiple_thread: 4
max_cnt: 75
freq: 30                # frequence (Hz) of publish tracking result. At least 10Hz for good estimation.
max_solver_time: 0.02  # max solver itration time (ms), to guarantee real time
max_num_iterations: 4   # max solver itrations, to guarantee real time
```

## Installation
Please follow original [VINS FUSION GPU](https://github.com/pjrambo/VINS-Fusion-gpu). The installation process is identical. You may need vitrual memory to compile the program.

## Acknowledgment
The Jetson devices in our experiment is supported by NVIDIA Jetson Nano 2GB Developer Kit Grant Program
