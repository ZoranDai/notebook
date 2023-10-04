# Raw GNSS + Lidar + Camera + IMU
## 论文阅读
### 1. Raw GNSS的使用
pseudorange + carrier 
1. 开源：[Factor Graph Fusion of Raw GNSS Sensing with IMU and Lidar for Precise Robot Localization without a Base Station.](https://github.com/JonasBchrt/raw-gnss-fusion)
2. 未开源：[Continuous and Precise Positioning in Urban Environments by Tightly Coupled Integration of GNSS, INS and Vision](https://ieeexplore.ieee.org/document/9866851)
### 2. 退化处理
1. 部分开源 INS-centric + Visual Outlier Culling [IC-GVINS: A Robust, Real-time, INS-Centric GNSS-Visual-Inertial Navigation System for Wheeled Robot](https://github.com/i2Nav-WHU/IC-GVINS)

### 3. lidar-Camera-IMU Fusion
1. 基于因子图 [LVI-SAM](https://github.com/TixiaoShan/LVI-SAM) [易用版本](https://github.com/Cc19245/LVI-SAM-Easyused)
2. 基于滤波 [R3live](https://github.com/hku-mars/r3live)
## 可以尝试改进的方向
### 1. Raw GNSS + Lidar + Camera + IMU 多传感器融合框架的提出（IESKF）
Raw GNSS 的使用 基于1
多传感器融合框架 基于3.2(相比与因子图优化，更加熟悉滤波的方法，对fastlio2有一定熟悉)
### 2. 关于退化判断的改进（lidar/Camera/GNSS）
Camera基于2.1

Lidar？

GNSS应该有对应的信号
