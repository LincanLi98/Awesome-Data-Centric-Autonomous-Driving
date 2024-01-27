# Awesome Data-Centric Autonomous Driving [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

**This is the official repository of our survey paper**:[Data-Centric Evolution in Autonomous Driving: A Comprehensive Survey of Big Data System, Data Mining, and Closed-Loop Technologies](https://arxiv.org/abs/2401.12888)

## Category
- [1. Motivation and Background of Data-Driven Autonomous Driving(background)](#1-Motivation-and-Background-of-Data-Driven-Autonomous-Driving)
  - [1.1 Reasons of Data-Driven Autonomous Driving](#11-Reasons-of-Data-Driven-Autonomous-Driving)
  - [1.2 Performance Upper Bound of Autonomous Driving Algorithms](#12-Performance-Upper-Bound-of-Autonomous-Driving-Algorithms)
- [2. Milestone Development of Autonomous Driving Datasets](#2-Milestone-Development-of-Autonomous-Driving-Datasets)
  - [2.1 Milestone Generation of AD Datasets](#21-Milestone-Generation-of-AD-Datasets)
  - [2.2 Dataset Acquisition, Settings, and Key Features](#22-Dataset-Acquisition-Settings-and-Key-Features)
  - [2.3 Public Leaderboard of Related Autonomous Driving Tasks](#23-Public-Leaderboard-of-Related-Autonomous-Driving-Tasks)
    - [2.3.1 Perception Task Leaderboard](#24-Perception-Task-Leaderboard)
    - [2.3.2 Prediction Task Leaderboard](#25-Prediction-Task-Leaderboard)
    - [2.3.3 Planning Task Leaderboard](#26-Planning-Task-Leaderboard)
  - [2.4 Awesome Challenging AD Task Solutions](24-Awesome-Challenging-AD-Task-Solutions)
    - [2.4.1 End2End AD Pipelines](#241-End2End-AD-Pipelines)
    - [2.4.2 AD Planning Task](#242-AD-Planning-Task)
    - [2.4.3 Bird-Eye-View Solutions](#243-Bird-Eye-View-Solutions)
- [3. Closed-Loop Data-Driven Autonomous Driving System](#3-Closed-Loop-Data-Driven-Autonomous-Driving-System)
  - [3.1 Characteristics of Closed-Loop Data-Driven AD Systems](#31-Characteristics-of-Closed-Loop-Data-Driven-AD-Systems)
  - [3.2 Industrial Representatives](#32-Industrial-Representatives)
  - [3.3 Key Technologies Involved in AD Big Data Systems](#33-Key-Technologies-Involved-in-AD-Big-Data-Systems)
  - [3.4 High-Fidelity AD Data Generation and Simulation](#34-High-Fidelity-AD-Data-Generation-and-Simulation)
  - [3.5 Auto-Labeling Methods for Autonomous Driving Big Data](#35-Auto-Labeling-Methods-for-Autonomous-Driving-Big-Data)
    - [3.5.1 Autonomous Driving Data Labeling Pipelines \& Characteristics](#351-Autonomous-Driving-Data-Labeling-Pipelines-Characteristics)
    - [3.5.2 Auto-labeling Methods from Basic Task to High-Level Standards](#352-Auto-labeling-Methods-from-Basic-Task-to-High-Level-Standards)
    - [3.5.3 Open Source Auto-Labeling Tools and Platforms](#353-Open-Source-Auto-Labeling-Tools-and-Platforms)
    - [3.5.4 Data Mining for Autonomous Driving](#354-Data-Mining-for-Autonomous-Driving)
    - [3.5.5 Active Learning for AD Big Data System](#355-Active-Learning-for-AD-Big-Data-System)

- [4. Discussion \& Future Research Directions](#4-Discussion-Future-Research-Directions)
  - [4.1 New Autonomous Driving Datasets at 3rd Generation and Beyond](#41-New-Autonomous-Driving-Datasets-at-3rd-Generation-and-Beyond)
  - [4.2 Hardware Supports for Autonomous Driving Algorithms](#42-Hardware-Supports-for-Autonomous-Driving-Algorithms)
  - [4.3 Personalized Autonomous Driving Recommendation based on User Behavior Data](#43-Personalized-Autonomous-Driving-Recommendation-based-on-User-Behavior-Data)
  - [4.4 Data Security and Trustworthy Autonomous Driving](#44-Data-Security-and-Trustworthy-Autonomous-Driving)


## 1. Motivation and Background of Data-Driven Autonomous Driving
### 1.1 Reasons of Data-Driven Autonomous Driving
Most of the collected AD big data comes from normal driving scenarios, of which we already have huge amount of similar samples in the database. But the ambition of Data-Centric Autonomous Driving lies in the **automatic observing of long-tail distribution challenging scenarios**, and the **self-evolution of AD intelligent algorithms/models**.

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/1-1_Long_Tail_Distribution.png" width="800">

### 1.2 Performance Upper Bound of Autonomous Driving Algorithms
Coming to year 2024, we are approaching the performance upper-bound of Autonomous Driving models. The key to break through the model performance upper-bound lies in Data-Centric Autonomous Driving Technologies: how we collect/labeling/store/utilize the tremendous & dynamic upgrading AD big data, how we employ various data-driven technologies in AD algorithms, and how we build our Data-Centric AD Platforms.

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/1-2_Illustration-of-AD-Model-Performance-Upper-Bound.png" width="700">

There are three key insights regarding the switch from Model-centric to Data-centric autonomous driving:
- First, existing rule-based methodologies fail to address the problem, even in planning and decision-making tasks which are previously considered as their strength.
- Second, closed-loop data-driven approach is indispensable for advanced AD algorithm development and deployment, with an emphasize on automatically alleviating long-tail distribution problem. 
- Third, we should re-consider the way of collecting, storing, and utilizing the massive autonomous driving data. Data collection should across all types of essential sensors equipped on AVs, not only camera recorded driving videos. During the storage and utilization procedure, information privacy, anonymity, and security should be guaranteed.

## 2. Milestone Development of Autonomous Driving Datasets
### 2.1 Milestone Generation of AD Datasets
The evolution of autonomous driving datasets mirrors the technological advancements and growing ambitions in the field. Early endeavors in the late 20th century, such as the MIT's AVT Research and UC Berkeley's PATH Program, laid the groundwork with basic sensor data, but were limited by the technology level of the era. There has been a significant leap forward over the last two decades, fueled by advancements in sensor technology, computational power, and sophisticated machine learning algorithms. In 2014, the Society of Automotive Engineers (SAE) announced a systematic six-level (L0-L5) autonomous driving system to the public, which has been widely recognized by autonomous driving R&D progress. Empowered by deep learning, computer vision-based methods have dominated intelligent perception. Deep reinforcement learning and its variants have provided crucial improvements in intelligent planning and decision-making. More recently, Large Language Models (LLMs) and Vision Language Models (VLMs) showcase their strong capability of scene understanding, driving behavior reasoning & prediction, and intelligent decision making, which open up new possibilities for future development of autonomous driving.

The **Figure** below illustrates the milestone development of Open-Source autonomous driving datasets following the chronological order.
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/Figure2-Milestone-Generation-of-OpenSource-AD-Datasets.png" width="1000">

Here is the related grand challenges mentioned with the famous datasets (the links cannot be normally displayed via figure)
| Dataset | KITTI | CityScapes | BDD 100K | Apolloscape | NuScenes | Waymo | Argoverse 1 | Lyft L5| NuPlan |  Argoverse 2| DriveLM|Generative AI Empowered Big Data|
|---------|-------|-------|-------|-------|-------|-------|-------|-------|--------|--------|--------|--------|
| **Open Challenges**|[KITTI Vision Benchmark Suite](https://www.cvlibs.net/datasets/kitti/)|[Cityscapes Benchmark Suite](https://www.cityscapes-dataset.com/benchmarks/)|[CVPR 2022 BDD100K Challenges](https://cvpr2022.wad.vision/)<br>[CVPR 2023 BDD100K Challenges](https://cvpr2023.wad.vision/)|[Apollospace Challenges & Leaderboard](https://apolloscape.auto/leader_board.html)|[Challenge at CVPR 2023 Autonomous Driving Workshop](https://opendrivelab.com/AD23Challenge.html)<br>[NuScenes Tracking Task](https://www.nuscenes.org/tracking?externalData=all&mapData=all&modalities=Any)<br>[NuScenes panoptic challenge](https://www.nuscenes.org/tracking?externalData=all&mapData=all&modalities=Any)|[Waymo Open Dataset 2023 Challenges](https://waymo.com/blog/2023/03/driving-research-forward-waymo-open/)<br>[Waymo Open Dataset Challenges on CVPR 2023 WAD Workshop](https://cvpr2023.wad.vision/)|[Argoverse Challenges at CVPR 2023 WAD Workshop](https://www.youtube.com/watch?v=X8HWCuQ7Hj0)<br>[Argoverse Challenges at CVPR 2022 WAD Workshop] (https://cvpr2022.wad.vision/)|[Lyft Motion Prediction for AVs](https://www.kaggle.com/c/lyft-motion-prediction-autonomous-vehicles)|[The 2023 nuPlan Planning Challenge at CVPR 2023](https://motional.com/news/2023-nuplan-challenge)|[Argoverse Challenges at CVPR 2023 WAD Workshop](https://www.youtube.com/watch?v=X8HWCuQ7Hj0)<br>[Argoverse 2: End-to-End Forecasting Challenge](https://eval.ai/web/challenges/challenge-page/2006/overview)| / | /  |

### 2.2 Dataset Acquisition,Settings,and Key Features
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/Table1-Summary-of-Influential-Perception-Dataset.png" width="1000">

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/Table2-Summary-of-Influential-Pred-Plan-Dataset.png" width="1000">

AV Sensor-Suite Equipment and Settings for Real world Data Acquisition, Take the benchmark **KITTI** & **NuScenes** as examples:
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/KITTI_Dataset_Acquisition_Settings.png" width="1000">

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/NuScenes_Dataset_Acquisition_Settings.png" width="1000">

### 2.3 Public Leaderboard of Related Autonomous Driving Tasks
#### 2.3.1 Perception Task Leaderboard
| 3D Object Tracking | 3D Object Detection|Image Semantic Segmentation|LiDAR Semantic Segmentation|Panoptic Segmentation|Lane Detection|LiDAR Point-Cloud Retrieval|
|-------|-------|-------|-------|-------|-------|-------|
| [NuScenes 3D Multi-Object Tracking](https://paperswithcode.com/sota/3d-multi-object-tracking-on-nuscenes) | [KITTI 3D Object Detection](https://paperswithcode.com/sota/3d-object-detection-on-kitti-cars-moderate)|[Cityscapes Semantic Segmentation](https://paperswithcode.com/sota/semantic-segmentation-on-cityscapes)|[SemanticKITTI 3D Semantic Segmentation](https://paperswithcode.com/sota/3d-semantic-segmentation-on-semantickitti)|[Cityscapes Panoptic Segmentation](https://paperswithcode.com/sota/video-panoptic-segmentation-on-cityscapes-vps)|[CULane Lane Detection](https://paperswithcode.com/sota/lane-detection-on-culane)|[Oxford RobotCar Point Cloud Retrieval](https://paperswithcode.com/sota/point-cloud-retrieval-on-oxford-robotcar)|
|[Argoverse 3D Object Tracking](https://paperswithcode.com/sota/3d-object-tracking-on-argoverse-cvpr-2020)| [BDD 100k Object Detection](https://paperswithcode.com/sota/traffic-object-detection-on-bdd100k-val)|[BDD100K val Multi-Object Segmentation](https://paperswithcode.com/sota/multi-object-tracking-and-segmentation-on-3)| [NuScenes LIDAR Semantic Segmentation](https://paperswithcode.com/sota/lidar-semantic-segmentation-on-nuscenes)|  /  |[TuSimple Lane Detection](https://paperswithcode.com/sota/lane-detection-on-tusimple)|   /  |
|[MOT17 Multi-Object Tracking](https://paperswithcode.com/sota/multi-object-tracking-on-mot17)|[Waymo 3D Object Detection on pedestrian](https://paperswithcode.com/sota/3d-object-detection-on-waymo-pedestrian)|[KITTI-360 Semantic Segmentation](https://paperswithcode.com/sota/semantic-segmentation-on-kitti-360)|   /  | Data  | [OpenLane Lane Detection](https://paperswithcode.com/sota/3d-lane-detection-on-openlane)| Data  |
|  /  |[Waymo 3D Object Detection on Vehicle](https://paperswithcode.com/sota/3d-object-detection-on-waymo-vehicle)|  /  |  /  |  /  |[CurveLanes Lane Detection](https://paperswithcode.com/sota/lane-detection-on-curvelanes)|  /  |
|  /  |  /  |   /  |  /  |  /  |  /  |  /  |
|  /  |  /  |  /   |  /  |  /  |  /  |  /  |

#### 2.3.2 Prediction Task Leaderboard
`In autonomous driving research, motion forecasting and trajectory prediction usually refer to the same task`

`However, there may be difference in whether we need to forecast the ego-vehicle's motion/trajectory or surrounding agents' motion/trajectory`

|     Motion Forecasting   /       Trajectory Prediction       | 
|--------------------------------------------------------------|
| [Apolloscape Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-apolloscape-1)| 
|[NuScenes Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-nuscenes)|
|[Argoverse 1 Motion Forecasting](https://paperswithcode.com/sota/motion-forecasting-on-argoverse-cvpr-2020)|
|[Waymo Open Motion Dataset for Motion Forecasting]([https://paperswithcode.com/sota/motion-forecasting-on-argoverse-cvpr-2020](https://paperswithcode.com/dataset/waymo-open-motion-dataset))|
|[Lyft Level 5 Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-lyft-level-5)|
|[Argoverse 2 Motion Forecasting](https://paperswithcode.com/dataset/argoverse-2-motion-forecasting)|

#### 2.3.3 Planning Task Leaderboard

| Planning Task | 
|---------------|
|[NuPlan Challenge LeaderBoard 2023](https://motional.com/news/2023-nuplan-challenge)| 
|[CARLA on Autonomous Driving Planning](https://paperswithcode.com/sota/autonomous-driving-on-carla-leaderboard)|
|[Motion Policy Networks](https://paperswithcode.com/dataset/motion-policy-networks)|


### 2.4 Awesome Challenging AD Task Solutions

This is an ongoing project. The rest of this project will be finished within one week!

### Acknowledgements to Our Research Work
Thanks for the appreciation of our research. If you use part of the content of our research, please cite our work as follows:
```
@misc{li2024datacentric,
      title={Data-Centric Evolution in Autonomous Driving: A Comprehensive Survey of Big Data System, Data Mining, and Closed-Loop Technologies}, 
      author={Lincan Li and Wei Shao and Wei Dong and Yijun Tian and Qiming Zhang and Kaixiang Yang and Wenjie Zhang},
      year={2024},
      eprint={2401.12888},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}
```
