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
  comment: LVI-SAM中丢弃了使用IMU预积分模块预测值作为前端里程计的初始值，预测值全部来自视觉里程计，但是如果视觉里程计飞掉，则预测值将会使用纯IMU旋转预测，这对于低成本或是6轴IMU来说（LIO-SAM可以很容易适配6轴传感器，支持6轴IMU版本可以使用liorf）是很难得到一个好的预测值的，这里是不是应该优先使用IMU预积分得到的结果，而在检测到Lidar里程计退化时再使用视觉里程计进行预测和补偿，实际测试后发现这种方法仍然是可行的.
2. 基于滤波 [R3live](https://github.com/hku-mars/r3live)

### 4. 数据结构
[ivox](https://github.com/gaoxiang12/faster-lio)
## 可以尝试改进的方向
### 1. 因子图中加入raw GNSS因子（LVI-SAM）
参考1.1 需要自己搭建实验平台录制数据集

### 2. 关于退化判断的改进（lidar/Camera/GNSS）
退化程度与因子权重构建关系
Camera基于2.1

Lidar？

GNSS应该有对应的信号
### 3. LIO-SAM部分改进
李宇航师兄的方法

Fast-lio2/faster-lio

## Step list
### 1. 配置LVI-SAM环境并跑通
### 2. 魔改其中的LIO，并熟悉框架
### 3. 构建退化程度与各个因子间的关系
### 4. 添加IMU预积分初始化模块并对比效果
### 5. 添加Raw GNSS因子
