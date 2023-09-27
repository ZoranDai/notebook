# Raw GNSS + Lidar + Camera + IMU
## 论文阅读
### 1. Raw GNSS的使用
pseudorange + carrier 
1. 开源：[Factor Graph Fusion of Raw GNSS Sensing with IMU and Lidar for Precise Robot Localization without a Base Station.](https://github.com/JonasBchrt/raw-gnss-fusion)
2. 未开源：[Continuous and Precise Positioning in Urban Environments by Tightly Coupled Integration of GNSS, INS and Vision](https://ieeexplore.ieee.org/document/9866851)
### 2. 退化处理
1. 部分开源 INS-centric + Visual Outlier Culling [IC-GVINS: A Robust, Real-time, INS-Centric GNSS-Visual-Inertial Navigation System for Wheeled Robot](https://github.com/i2Nav-WHU/IC-GVINS)
## 可以尝试改进的方向
### 1. Raw GNSS + Lidar + Camera + IMU 多传感器融合框架的提出（因子图优化）
基于1
### 2. 关于退化判断的改进（lidar/Camera/GNSS）
Camera基于2.1

Lidar？

GNSS应该有对应的信号
