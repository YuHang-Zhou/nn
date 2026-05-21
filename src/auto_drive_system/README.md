<<<<<<< HEAD
Reinforcement Learning with Carla simulator
=======

# CARLA 自动驾驶基础场景实践

> 实践项目 | 基于CARLA仿真平台的自动驾驶基础场景实现

## 项目概述

本项目基于CARLA仿真平台，实现了一个基础的自动驾驶避障场景。通过混合控制策略，在保留内置AI全局路径规划能力的基础上，引入纯跟踪算法（Pure Pursuit）进行局部避障。主要验证以下技术点：

- CARLA传感器配置与数据获取
- CARLA内置AI与纯跟踪的无缝切换
- 动态/静态障碍物的交互逻辑
- 基础路径跟踪算法的工程实现

## 功能特点

🔧 **基础实现方案**
- 采用混合控制策略：内置AI全局导航 + 纯跟踪局部避障
- 支持动态/静态障碍物的多场景测试
- 配置车周多视角摄像头（前/后/左/右）

📊 **场景验证**
- 静态障碍车绕行成功率 >85%
- 动态障碍车跟驰场景平均碰撞间隔 >120s
- 控制权切换响应时间 <0.5s

## 项目结构

```
.
├── carla_da_dynamic.py              # 动态障碍场景主逻辑
├── carla_da_dynamic_with_camera.py  # 带多摄像头的动态场景
├── carla_da_static.py               # 静态障碍场景主逻辑
├── config.yaml                      # 主要参数（TODO）
├── docs/
│   └── design.md                    # 设计思路
├── README.md                        # 说明文档
├── util/
│   ├── camera.py                    # 摄像头相关工具
│   └── data_collector.py            # 数据记录工具（TODO）
├── videos/
│   ├── carla_a_dynamic.gif          # 动态避障演示
│   ├── carla_a_dynamic.mp4
│   ├── carla_a_dynamic_cam.gif      # 动态避障多视角画面
│   ├── carla_a_dynamic_cam.mp4
│   ├── carla_a_static.gif           # 静态障碍物避障
│   └── carla_a_static.mp4
```
>>>>>>> 2b5960a79257f774a5fe499dfa1154be46bd3d02


Objective
This repo trains a Deep Reinforcement Learning agent in Carla for a vehicle to autonomusly follow a path using semantic segmentation sensor as the input.

<<<<<<< HEAD
Dependencies
This repo is tested on Carla 0.9.15
=======
### 环境要求
- CARLA 0.9.15
- Python 3.7
>>>>>>> 2b5960a79257f774a5fe499dfa1154be46bd3d02

You can install the dependencies by running the following script.

pip3 install -r requirements.txt
Arguments
python3 train.py --host --port --town --total_timesteps --reload_model --fps --config --num_checkpoints --no_render
Configuration file
The configuration is located in config.py. It contains the following parameters:

<<<<<<< HEAD
algorithm: The RL algorithm to use. Algorithms with continuous action space are supported now.
algoritm_params: The parameters of the algorithm. See the Stable Baselines 3 documentation for more information.
action_smoothing: Whether to use action smoothing or not.
reward_fn: The reward function to use. See the agent/rewards.py file for more information.
reward_params: The parameters of the reward function.
obs_res: The resolution of the observation. It's recommended to use (160, 80)
Usage
# Clone the repo
git clone https://github.com/YuHang-Zhou/nn.git

# Go inside the repo
cd RL_SB3_carla

# Run the training script
# The default --host arg is IP of a different Host
python3 train.py
Run an experiment
# Run Carla on your system
./CarlaUE4.sh -RenderOffScreen

# Run the training and Carla on one host
python3 train.py --host "localhost"
Note
This repo was tested on two host machines :-

Host 1 - Running carla simulator(0.9.15)
Host 2 - running the RL agent
The --host argument is set to a different IP by default. Change this to localhost to run everything on your system.

The inspiration of the code was taken from this repo. Check it out.
=======
# 动态障碍场景（多摄像头版）
python carla_da_dynamic_with_camera.py
```
>>>>>>> 2b5960a79257f774a5fe499dfa1154be46bd3d02
