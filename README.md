# 矿山场景可行驶区域拟合
## 背景介绍
自动驾驶的相关研究通常在城市场景中进行，其道路比较平坦且具有较明显的边界线，因此车辆的可行驶区域可以较为容易地获取。而矿山场景往往会出现路面崎岖、凹凸不平、道路边界线不清晰的问题，从而导致我们难以准确获取车辆的可行驶区域。

## 解决方案
### 基于Patchwork++
- 针对道路上下坡较多，难以使用统一地面拟合，因此使用局部地面拟合的方法
- 针对lidar点云距离lidar越远点云数量越少的分布情况，使用扇形区域分割方法
### 创新点
- 在局部地面拟合的具体实现中，使用临近区域拟合的参数（高程、法向量等）判断分割当前区域的可行驶区域
- 针对较远区域lidar分割效果不稳定的问题，使用相邻帧对比的方法进行稳定性判断

### 待调研
- 受[A Fast Point Cloud Ground Segmentation Approach Based on Coarse-To-Fine Markov Random Field](https://ieeexplore.ieee.org/document/9410344)启发，可以

### 对比算法
- PCA
- RANSAC
- PatchWork
- Patchwork++

### 数据集
- 点云标注（是否为可行驶区域）

A Fast Point Cloud Ground Segmentation Approach Based on Coarse-To-Fine Markov Random Field
