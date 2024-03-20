# Awesome Data-Centric Autonomous Driving [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

**This project gathering & summarize Data-Driven Autonomous Driving Solutions from both Academic SOTA models, and Industrial Frontier solutions. It's also the official repository of our survey paper**: [Data-Centric Evolution in Autonomous Driving: A Comprehensive Survey of Big Data System, Data Mining, and Closed-Loop Technologies](https://arxiv.org/abs/2401.12888)

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
    - [2.3.4 LLM/VLM Enhanced Autonomous Driving Benchmark Dataset](#27-LLM/VLM-Task-Leaderboard)
  - [2.4 Awesome Challenging AD Task Solutions](24-Awesome-Challenging-AD-Task-Solutions)
    - [2.4.1 End2End AD Pipelines](#241-End2End-AD-Pipelines)
    - [2.4.2 AD Planning Task](#242-AD-Planning-Task)
    - [2.4.3 High-Fidelity Autonomous Driving Data Generation](#243-Autonomous-Driving-Data-Generation)
    - [2.4.4 Bird-Eye-View Solutions](#244-Bird-Eye-View-Solutions)
- [3. Closed-Loop Data-Driven Autonomous Driving System](#3-Closed-Loop-Data-Driven-Autonomous-Driving-System)
  - [3.1 Characteristics of Closed-Loop Data-Driven AD Systems](#31-Characteristics-of-Closed-Loop-Data-Driven-AD-Systems)
  - [3.2 Industrial Representatives](#32-Industrial-Representatives)
  - [3.3 Key Technologies Involved in AD Big Data Systems](#33-Key-Technologies-Involved-in-AD-Big-Data-Systems)
  - [3.4 High-Fidelity AD Data Generation and Simulation](#34-High-Fidelity-AD-Data-Generation-and-Simulation)
  - [3.5 Auto-Labeling Methods for Autonomous Driving Big Data](#35-Auto-Labeling-Methods-for-Autonomous-Driving-Big-Data)
    - [3.5.1 Autonomous Driving Data Labeling Pipelines \& Characteristics](#351-Autonomous-Driving-Data-Labeling-Pipelines-Characteristics)
    - [3.5.2 Auto-labeling Methods from Basic Task to High-Level Standards](#352-Auto-labeling-Methods-from-Basic-Task-to-High-Level-Standards)
    - [3.5.3 Open Source Auto-Labeling Tools and Platforms](#353-Open-Source-Auto-Labeling-Tools-and-Platforms)
  - [3.6 Autonomous Driving Sensor Suite Calibration Tools](#36-Autonomous-Driving-Sensor-Suite-Calibration-Tools)
  - [3.7 Autonomous Driving Visualization Tools](#37-Autonomous-Driving-Visualization-Tools)

- [4. Discussion \& Future Research Directions](#4-Discussion-Future-Research-Directions)
  - [4.1 New Autonomous Driving Datasets at 3rd Generation and Beyond](#41-New-Autonomous-Driving-Datasets-at-3rd-Generation-and-Beyond)
  - [4.2 Hardware Supports for Autonomous Driving Algorithms](#42-Hardware-Supports-for-Autonomous-Driving-Algorithms)
  - [4.3 Personalized Autonomous Driving Recommendation based on User Behavior Data](#43-Personalized-Autonomous-Driving-Recommendation-based-on-User-Behavior-Data)
  - [4.4 Data Security and Trustworthy Autonomous Driving](#44-Data-Security-and-Trustworthy-Autonomous-Driving)


## 1. Motivation and Background of Data-Driven Autonomous Driving
### 1.1 Reasons of Data-Driven Autonomous Driving
Most of the collected AD big data comes from normal driving scenarios, of which we already have huge amount of similar samples in the database. But the ambition of Data-Centric Autonomous Driving lies in the **automatic observing of long-tail distribution challenging scenarios**, and the **self-evolution of AD intelligent algorithms/models**.

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/1-1_Long_Tail_Distribution.png" width="600">

### 1.2 Performance Upper Bound of Autonomous Driving Algorithms
Coming to year 2024, we are approaching the performance upper-bound of Autonomous Driving models. The key to break through the model performance upper-bound lies in Data-Centric Autonomous Driving Technologies: how we collect/labeling/store/utilize the tremendous & dynamic upgrading AD big data, how we employ various data-driven technologies in AD algorithms, and how we build our Data-Centric AD Platforms.

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/1-2_Illustration-of-AD-Model-Performance-Upper-Bound.png" width="600">

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
| 3D Object Tracking | 3D Object Detection|Video Semantic Segmentation|LiDAR Semantic Segmentation|Panoptic Segmentation|Lane Detection|LiDAR Point-Cloud Retrieval|Occupancy Prediction|
|-------|-------|-------|-------|-------|-------|-------|-------|
| [NuScenes 3D Multi-Object Tracking](https://paperswithcode.com/sota/3d-multi-object-tracking-on-nuscenes) | [KITTI 3D Object Detection](https://paperswithcode.com/sota/3d-object-detection-on-kitti-cars-moderate)|[Cityscapes Semantic Segmentation](https://paperswithcode.com/sota/semantic-segmentation-on-cityscapes)|[SemanticKITTI 3D Semantic Segmentation](https://paperswithcode.com/sota/3d-semantic-segmentation-on-semantickitti)|[Cityscapes Panoptic Segmentation](https://paperswithcode.com/sota/video-panoptic-segmentation-on-cityscapes-vps)|[CULane Lane Detection](https://paperswithcode.com/sota/lane-detection-on-culane)|[Oxford RobotCar Point Cloud Retrieval](https://paperswithcode.com/sota/point-cloud-retrieval-on-oxford-robotcar)|[Occ3D-nuScenes](https://paperswithcode.com/sota/prediction-of-occupancy-grid-maps-on-occ3d)|
|[Argoverse 3D Object Tracking](https://paperswithcode.com/sota/3d-object-tracking-on-argoverse-cvpr-2020)| [BDD 100k Object Detection](https://paperswithcode.com/sota/traffic-object-detection-on-bdd100k-val)|[BDD100K val Multi-Object Segmentation](https://paperswithcode.com/sota/multi-object-tracking-and-segmentation-on-3)| [NuScenes LIDAR Semantic Segmentation](https://paperswithcode.com/sota/lidar-semantic-segmentation-on-nuscenes)|  /  |[TuSimple Lane Detection](https://paperswithcode.com/sota/lane-detection-on-tusimple)|   /   |   /    |
|[MOT17 Multi-Object Tracking](https://paperswithcode.com/sota/multi-object-tracking-on-mot17)|[Waymo 3D Object Detection on pedestrian](https://paperswithcode.com/sota/3d-object-detection-on-waymo-pedestrian)|[KITTI-360 Semantic Segmentation](https://paperswithcode.com/sota/semantic-segmentation-on-kitti-360)|   /  |   /   | [OpenLane Lane Detection](https://paperswithcode.com/sota/3d-lane-detection-on-openlane)|   /   |    /    |
|  /  |[Waymo 3D Object Detection on Vehicle](https://paperswithcode.com/sota/3d-object-detection-on-waymo-vehicle)|  /  |  /  |   /  |[CurveLanes Lane Detection](https://paperswithcode.com/sota/lane-detection-on-curvelanes)|   /   |   /   |
|  /  |  /  |   /  |  /  |  /  |  /  |  /  |   /   |
|  /  |  /  |  /   |  /  |  /  |  /  |  /  |   /   |

#### 2.3.2 Prediction Task Leaderboard
In autonomous driving research, `motion forecasting` and `trajectory prediction` usually refer to the same task. However, there may be differences in whether we need to forecast the `ego-vehicle's motion/trajectory` or `surrounding agents' motion/trajectory`.

|     Motion Forecasting   /       Trajectory Prediction       | 
|--------------------------------------------------------------|
| [Apolloscape Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-apolloscape-1)| 
|[NuScenes Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-nuscenes)|
|[Argoverse 1 Motion Forecasting](https://paperswithcode.com/sota/motion-forecasting-on-argoverse-cvpr-2020)|
|[Waymo Open Motion Dataset for Motion Forecasting](https://paperswithcode.com/dataset/waymo-open-motion-dataset)|
|[Lyft Level 5 Trajectory Prediction](https://paperswithcode.com/sota/trajectory-prediction-on-lyft-level-5)|
|[Argoverse 2 Motion Forecasting](https://paperswithcode.com/dataset/argoverse-2-motion-forecasting)|

#### 2.3.3 Planning Task Leaderboard

| Planning Task | 
|---------------|
|[NuPlan Challenge LeaderBoard 2023](https://motional.com/news/2023-nuplan-challenge)| 
|[CARLA on Autonomous Driving Planning](https://paperswithcode.com/sota/autonomous-driving-on-carla-leaderboard)|
|[Motion Policy Networks](https://paperswithcode.com/dataset/motion-policy-networks)|


#### 2.3.4 LLM/VLM Enhanced Autonomous Driving Benchmark Dataset

| LLM/VLM Enhanced AD Benchmarks| 
|---------------|
|[DriveLM](https://github.com/OpenDriveLab/DriveLM/tree/main)| 
|[LaMPilot](https://arxiv.org/pdf/2312.04372.pdf)|

### 2.4 Awesome Challenging AD Task Solutions

#### 2.4.1 End2End AD Pipelines
1.[(CVPR 2023) Planning-Oriented Autonomous Driving](https://openaccess.thecvf.com/content/CVPR2023/html/Hu_Planning-Oriented_Autonomous_Driving_CVPR_2023_paper.html)

2.[(ICCV 2023) DriveAdapter: Breaking the Coupling Barrier of Perception and Planning in End-to-End Autonomous Driving](https://openaccess.thecvf.com/content/ICCV2023/html/Jia_DriveAdapter_Breaking_the_Coupling_Barrier_of_Perception_and_Planning_in_ICCV_2023_paper.html)

3.[DriveGPT4: Interpretable End-to-end Autonomous Driving via Large Language Model](https://arxiv.org/abs/2310.01412)

4.[(Baidu) Rethinking the Open-Loop Evaluation of End-to-End Autonomous Driving in nuScenes](https://arxiv.org/abs/2305.10430)

5.[(CVPR 2023) ReasonNet: End-to-End Driving With Temporal and Global Reasoning](https://openaccess.thecvf.com/content/CVPR2023/html/Shao_ReasonNet_End-to-End_Driving_With_Temporal_and_Global_Reasoning_CVPR_2023_paper.html)

6.[(CVPR 2023) Coaching a Teachable Student](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Coaching_a_Teachable_Student_CVPR_2023_paper.html)

7.[DriveLM: Driving with Graph Visual Question Answering](https://arxiv.org/abs/2312.14150)

8.[(CoRL) Safety-Enhanced Autonomous Driving Using Interpretable Sensor Fusion Transformer](https://proceedings.mlr.press/v205/shao23a.html)

9.[(ECCV 2022) ST-P3: End-to-End Vision-Based Autonomous Driving via Spatial-Temporal Feature Learning](https://link.springer.com/chapter/10.1007/978-3-031-19839-7_31)

10.[(ICLR 2023) Policy Pre-training for Autonomous Driving via Self-supervised Geometric Modeling](https://arxiv.org/abs/2301.01006)

11.[(NeurIPS 2022) Trajectory-guided Control Prediction for End-to-end Autonomous Driving: A Simple yet Strong Baseline](https://proceedings.neurips.cc/paper_files/paper/2022/hash/286a371d8a0a559281f682f8fbf89834-Abstract-Conference.html)


#### 2.4.2 AD Planning Task
1.[(ICLR 2024) Dilu: A knowledge-driven approach to autonomous driving with large language models](https://arxiv.org/abs/2309.16292)

2.[(ICRA 2023) TrafficBots: Towards World Models for Autonomous Driving Simulation and Motion Prediction](https://arxiv.org/abs/2303.04116)

3.[(1st Solution on 2023 nuPlan Challenge) Parting with Misconceptions about Learning-based Vehicle Motion Planning](https://arxiv.org/pdf/2306.07962.pdf)

4.[(Horizon Robotics--2nd Solution on 2023 nuPlan Challenge) Imitation with Spatial-Temporal Heatmap:2nd Place Solution for NuPlan Challenge](https://arxiv.org/abs/2306.15700)

5.[(3rd Solution on 2023 nuPlan Challenge) An Imitation Learning Method with Data Augmentation and Post Processing for Planning in Autonomous Driving](https://opendrivelab.com/e2ead/AD23Challenge/Track_4_pegasus_weitao.pdf)

6.[FusionPlanner: A Multi-task Motion Planner for Mining Trucks via Multi-sensor Fusion](https://arxiv.org/abs/2308.06931)

7.[(Shanghai AI Lab) Gameformer planner: A learning-enabled interactive prediction and planning framework for autonomous vehicles](https://opendrivelab.com/e2ead/AD23Challenge/Track_4_AID.pdf)

8.[LLM-Assist: Enhancing Closed-Loop Planning with Language-Based Reasoning](https://arxiv.org/abs/2401.00125)

9.[VLP: Vision Language Planning for Autonomous Driving](https://arxiv.org/abs/2401.05577)


#### 2.4.3 High-Fidelity Autonomous Driving Data Generation

1.[(CVPR2024) Panacea: Panoramic and Controllable Video Generation for Autonomous Driving](https://panacea-ad.github.io/)
2.[(CVPR2024) Editable Scene Simulation for Autonomous Driving via LLM-Agent Collaboration](https://yifanlu0227.github.io/ChatSim/)
3.[BerfScene: Bev-conditioned Equivariant Radiance Fields for Infinite 3D Scene Generation](https://arxiv.org/abs/2312.02136)



#### 2.4.4 Bird-Eye-View (BEV) Solutions
1.[(TPAMI) Delving Into the Devils of Bird's-Eye-View Perception: A Review, Evaluation and Recipe](https://ieeexplore.ieee.org/abstract/document/10321736)

2.[(CVPR 2023) BEVFormer v2: Adapting Modern Image Backbones to Bird's-Eye-View Recognition via Perspective Supervision](https://openaccess.thecvf.com/content/CVPR2023/html/Yang_BEVFormer_v2_Adapting_Modern_Image_Backbones_to_Birds-Eye-View_Recognition_via_CVPR_2023_paper.html)

3.[(ICRA 2023) BEVFusion: Multi-Task Multi-Sensor Fusion with Unified Bird's-Eye View Representation](https://ieeexplore.ieee.org/abstract/document/10160968)

4.[(ICCV 2023) Fb-bev: Bev representation from forward-backward view transformations](https://openaccess.thecvf.com/content/ICCV2023/html/Li_FB-BEV_BEV_Representation_from_Forward-Backward_View_Transformations_ICCV_2023_paper.html)

5.[(ICCV 2023) FocalFormer3D: Focusing on Hard Instance for 3D Object Detection](https://openaccess.thecvf.com/content/ICCV2023/html/Chen_FocalFormer3D_Focusing_on_Hard_Instance_for_3D_Object_Detection_ICCV_2023_paper.html)

6.[(ICCV 2023) Bird's-Eye-View Scene Graph for Vision-Language Navigation](https://openaccess.thecvf.com/content/ICCV2023/html/Liu_Birds-Eye-View_Scene_Graph_for_Vision-Language_Navigation_ICCV_2023_paper.html)

7.[(ECCV 2022) BEVFormer: Learning Bird’s-Eye-View Representation from Multi-camera Images via Spatiotemporal Transformers](https://link.springer.com/chapter/10.1007/978-3-031-20077-9_1)

8.[BEVerse: Unified Perception and Prediction in Birds-Eye-View for Vision-Centric Autonomous Driving](https://arxiv.org/abs/2205.09743)

9.[(CVPR 2022) Exploiting Temporal Relations on Radar Perception for Autonomous Driving](https://openaccess.thecvf.com/content/CVPR2022/html/Li_Exploiting_Temporal_Relations_on_Radar_Perception_for_Autonomous_Driving_CVPR_2022_paper.html)

10.[(T-IV) BEV-V2X: Cooperative Birds-Eye-View Fusion and Grid Occupancy Prediction via V2X-Based Data Sharing](https://ieeexplore.ieee.org/abstract/document/10179171)

11.[(CVPR 2023) UniDistill: A Universal Cross-Modality Knowledge Distillation Framework for 3D Object Detection in Bird's-Eye View](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_UniDistill_A_Universal_Cross-Modality_Knowledge_Distillation_Framework_for_3D_Object_CVPR_2023_paper.html)

12.[(ICCV 2023) UniTR: A Unified and Efficient Multi-Modal Transformer for Bird's-Eye-View Representation](https://openaccess.thecvf.com/content/ICCV2023/html/Wang_UniTR_A_Unified_and_Efficient_Multi-Modal_Transformer_for_Birds-Eye-View_Representation_ICCV_2023_paper.html)

## 3. Closed-Loop Data-Driven Autonomous Driving System
We're now shifting from the previous era of software & algorithm defined autonomous driving towards the new inspiring era of big data-driven & intelligent model collaborative autonomous driving. Closed-loop data-driven systems aim to bridge the gap between AD algorithm training and their real-world application/deployment. Unlike traditional open-loop methods, where models are passively trained on datasets collected from human client driving or road testing, closed-loop systems interact dynamically with the real environment. This approach addresses the distribution shifting challenge--where behavior learned from static datasets may not translate to the dynamic nature of real-world driving scenarios. Closed-loop systems allow AVs to learn from interactions and adapt to new situations, improving through iterative cycles of action and feedback. 

### 3.1 Characteristics of Closed-Loop Data-Driven AD Systems
- These pipelines usually follow a workflow circle that includes: (I) data acquisition, (II) data storage, (III) data selection & preprocessing, (IV) data labeling, (V) AD model training, (VI) simulation/test validation, and (VII) real-world deployment. 
- For the design of closed-loops within the system, existing solutions either choose separately set "Data Close-Loop" & "Model Close-Loop", or separately set cycles for different stages: "Close Loop during R&D stage" and "Close Loop during deployment stage".
- Aside from that, the industry also emphasizes the long-tail distribution problem of real-world AD datasets and the challenges when dealing with corner case. Tesla and NVIDIA are industry pioneers in this realm, and their data system architectures offer significant reference for the development of the field.

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-1_momenta_data_driven_planning.png" width="700">
The above figure is Momenta's full-stack data-driven AD pipeline, it clearly shows the transformation from classical rule-based planning to data-driven planning.

### 3.2 Industrial Representatives
`The contents presented below should not be construed as any form of recommendation or suggestion`
- [NVIDIA MagLev Platform](https://www.youtube.com/watch?v=HuIWTwE28QE)
- [Tesla AutoPilot Data Platform](https://www.youtube.com/watch?v=6x-Xb_uT7ts)
- [Momenta Data-Driven Flywheel Platform](https://www.momenta.ai/en/technology.html)
- [Horizon Robotics Closed-Loop Data Platform "AiDi"](https://en.horizon.cc/developers-tools-and-sw-stack/)
- [SenseAuto Empower Engine](https://www.sensetime.com/cn/product-detail?categoryId=51133699)
- [Baidu Closed-Loop Data System](https://www.autonomousvehicleinternational.com/news/robotaxis/baidu-apollo-day-expanded-robotaxi-operations-and-new-autonomous-driving-software-and-hardware.html)
- [XPENG ADAS Closed-Loop System](https://ir.xiaopeng.com/zh-hans/news-releases/news-release-details/xpeng-presents-next-gen-technology-architecture-sepa20)
- [Pony.ai AD Data Platform](https://pony.ai/business?lang=en)
- [Amazon Autonomous Mobility Data System](https://aws.amazon.com/automotive/autonomous-mobility/)

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-2-1_Tesla_close_loop.png" width="600">

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-2-2_Waymo_close_loop.png" width="600">

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-2-3_Horizon_robotics_close_loop.png" width="600">

<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-2-4_Baidu_Close_Loop_Data_System.jpg" width="600">

### 3.3 Key Technologies Involved in AD Big Data Systems
This is the schematic of the Key Technologies involved in Data-Driven Closed-Loop Autonomous Driving.
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-3_mindmap_key_technology_involved.png" width="550">

### 3.4 High-Fidelity AD Data Generation and Simulation
- Simulation on CARLA.
- **World Model**-based Methods.

### CARLA Simulation
[CARLA](https://carla.org//) is an open-source simulator for autonomous driving that enables the generation of AD data under various settings specified by the user. The advantage of CARLA lies in its flexibility, allowing users to create diverse road conditions, traffic scenarios, and weather dynamics. However, as a simulator, AD data generated by CARLA cannot fully mimic the real world physics and visual effects; the dynamic and complex characteristics of real driving environment are also not repre sented.

[(CoRL 2017) Carla: An open urban driving simulator.](https://proceedings.mlr.press/v78/dosovitskiy17a.html)

[KITTI-CARLA: a KITTI-like dataset generated by CARLA Simulator](https://arxiv.org/abs/2109.00892)

### 👍👍World Models for Autonomous Driving
**World Model can be defined as** an **AI system** that builds an internal representation of the environment it perceives, and uses the learned representation to simulate data or events within the environment. The objective of general world models are to represent and simulate various situations and interactions, like a mature human will encountered in the real-world.

I highly recommend you to read the source paper which propose the concept of "World Model" at here: [(NIPS 2018 Oral) World Models](https://arxiv.org/abs/1803.10122)
The authors also build an interactive website at [here](https://worldmodels.github.io/)

The fig below is originally created by `DALL·E`, which imagines the integration of World Model and Autonomous Driving.
<div align="center">
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-4-World-Model-in-Autonomous-Driving-Generated-by-DALLE.png" width="400">
</div>

At present, `World Models` have been employed in the following aspects of autonomous driving:

  (i) Traffic stream simulation & sensor data generation👍
  
  (ii) High-fidelity driving scene data generation👍
  
  (iii) Intelligent planning for AV👍

| (i)Traffic stream simulation & sensor data generation | 
|----------------------------------------------------|
|[TrafficBots: Towards world models for autonomous driving simulation and motion prediction](https://arxiv.org/abs/2303.04116)| 
|[(CMU & NVIDIA) Language-Guided Traffic Simulation via Scene-Level Diffusion](https://arxiv.org/abs/2306.06344)|
|[(Tsinghua) SurrealDriver: Designing Generative Driver Agent Simulation Framework in Urban Contexts based on Large Language Model](https://arxiv.org/abs/2309.13193)|

| (ii)High-fidelity driving scene data generation | 
|----------------------------------------------------|
|[(ICLR 2024) Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion](https://arxiv.org/abs/2311.01017)|
|[(wayve.ai) GAIA-1: A Generative World Model for Autonomous Driving](https://arxiv.org/abs/2309.17080)| 
|[(Giga AI & Tsinghua) DriveDreamer: Towards Real-world-driven World Models for Autonomous Driving](https://arxiv.org/abs/2309.09777)|
|[(Peking University) UniWorld: Autonomous Driving Pre-training via World Models](https://arxiv.org/abs/2308.07234)|
|[(MEGVII Technology) ADriver-I: A General World Model for Autonomous Driving](https://arxiv.org/abs/2311.13549)|

| (iii)Intelligent planning for AV | 
|----------------------------------------------------|
|[Driving into the Future: Multiview Visual Forecasting and Planning with World Model for Autonomous Driving](https://arxiv.org/abs/2311.17918)| 
|[(CoRL 2023) DayDreamer: World Models for Physical Robot Learning](https://proceedings.mlr.press/v205/wu23c.html)|
|[(ICML 23) Do Embodied Agents Dream of Pixelated Sheep: Embodied Decision Making using Language Guided World Modelling](https://arxiv.org/abs/2301.12050)|

### 3.5 Auto-Labeling Methods for Autonomous Driving Big Data
```
"LLMs can label data as well as humans, but 100x faster"--by [Refuel Team](https://www.refuel.ai/blog-posts/llm-labeling-technical-report)
```

Auto-labeling methods hold great promise in alleviating the intensive labor of manual annotation, improving the efficiency of AD data closed-loop cycle, and reducing the expenses. Classic auto-labeling tasks include scene classification & understanding. Recently, with the popularization of Bird's-Eye-View (BEV) perception methodology, the industrial standard for AD data labeling is also increasing, and the auto-labeling tasks are becoming more complicated. 

#### 3.5.1 Autonomous Driving Data Labeling Pipelines \& Characteristics
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-5-Mainstream-AD-Labeling-Pipelines.png" width="1000">

Existing data labeling pipelines can be characterized as three types, (1) Traditional handicraft labeling; (2) Semi-automatic labeling; (3) Fully auto-labeling approach. AD data labeling is usually considered as `Task/Model specific`. The figure above illustartes the detailed labeling procedures.

#### 3.5.2 Auto-labeling Methods from Basic Task to High-Level Standards
- Scene Classification & Understanding
- 3D Dynamic Object Auto-Labeling
- 3D Static Scene Auto-Labeling

#### Scene Classification & Understanding
[(NeurIPS 2023) OpenLane-V2: A Topology Reasoning Benchmark for Unified 3D HD Mapping](https://arxiv.org/abs/2304.10440)

[(CVPR 2023)OpenScene: 3D Scene Understanding With Open Vocabularies](https://openaccess.thecvf.com/content/CVPR2023/html/Peng_OpenScene_3D_Scene_Understanding_With_Open_Vocabularies_CVPR_2023_paper.html)

[Yolov8: A new state-of-the-art computer vision model, 2023.](https://docs.ultralytics.com/)

[(ICCV 2021) MGNet: Monocular Geometric Scene Understanding for Autonomous Driving](https://openaccess.thecvf.com/content/ICCV2021/html/Schon_MGNet_Monocular_Geometric_Scene_Understanding_for_Autonomous_Driving_ICCV_2021_paper.html)

[NLE-DM: Natural-Language Explanations for Decision Making of Autonomous Driving Based on Semantic Scene Understanding](https://ieeexplore.ieee.org/abstract/document/10144484)

[S3-Net: A Fast Scene Understanding Network by Single-Shot Segmentation for Autonomous Driving](https://dl.acm.org/doi/abs/10.1145/3470660)

[A novel scene classification model combining resnet based transfer learning and data augmentation with a filter](https://www.sciencedirect.com/science/article/abs/pii/S0925231219301833)

#### 3D Dynamic Object Auto-Labeling
[(Waymo 3D Auto-Labeling for LiDAR, CVPR 2021)Offboard 3D Object Detection From Point Cloud Sequences](https://openaccess.thecvf.com/content/CVPR2021/html/Qi_Offboard_3D_Object_Detection_From_Point_Cloud_Sequences_CVPR_2021_paper.html)

[(Uber Auto4D pipeline) Auto4D: Learning to Label 4D Objects from Sequential Point Clouds](https://arxiv.org/abs/2101.06586)

[(NeurIPS2023) AD-PT: Autonomous Driving Pre-Training with Large-scale Point Cloud Dataset](https://arxiv.org/abs/2306.00612)

[OpenAnnotate3D: Open-Vocabulary Auto-Labeling System for Multi-modal 3D Data](https://arxiv.org/abs/2310.13398)

#### 3D Static Scene Auto-Labeling

`Vision-based methods`

[(CVPR 2023) Offboard hd-map generation with multi-view consistency](https://openaccess.thecvf.com/content/ICCV2023/html/Xie_MV-Map_Offboard_HD-Map_Generation_with_Multi-view_Consistency_ICCV_2023_paper.html)

[Nemo: Neural map growing system for spatiotemporal fusion in bird’s-eye-view and bdd-map benchmark](https://arxiv.org/abs/2306.04540)

`LiDAR-based methods`

[VMA: Divide-and-Conquer Vectorized Map Annotation System for Large-Scale Driving Scene](https://arxiv.org/abs/2304.09807)

`Pretraining 3D scene reconstruction methods`

[Occ-bev: Multi-camera unified pre-training via 3d scene reconstruction.](https://arxiv.org/abs/2305.18829)

[(ICCV 2023) Scene as occupancy](https://openaccess.thecvf.com/content/ICCV2023/html/Tong_Scene_as_Occupancy_ICCV_2023_paper.html)

[(NeurIPS 2023) Ad-pt: Autonomous driving pre-training with large-scale point cloud dataset](https://arxiv.org/abs/2306.00612)

[(CVPR 2023) Also: Automotive lidar self-supervision by occupancy estimation](https://openaccess.thecvf.com/content/CVPR2023/html/Boulch_ALSO_Automotive_Lidar_Self-Supervision_by_Occupancy_Estimation_CVPR_2023_paper.html)



#### 3.5.3 Open Source Auto-Labeling Tools and Platforms

🚀(1) **[X-AnyLabeling](https://github.com/CVHub520/X-AnyLabeling)**: Effortless data labeling with AI support from Segment Anything and other awesome models.
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-5-3-X-AnyLabeling.png" width="350">
<br>
- [x] Support importing both **image** and **video** source data
- [x] **One-click export** functionality, supporting **multiple standard formats** including  including COCO-JSON, VOC-XML, YOLOv5 TXT, DOTA-TXT, and MOT-CSV
- [x] Supports multiple hardware environments (enable GPU inference) and cross platform applications (Windows, Linux, MacOS)
- [x] Support comprehensive SOTA deep learning models, including SAM, YoLo, etc.

<br>
<br>


🚀(2) **[AutoLabelImg](https://github.com/wufan-tb/AutoLabelImg)**: Multi-Function AutoAnnotate Tools
<br>
AutoLabelImg is based on labelImg, but add more useful annotation tools and functions, which enables:
- [x] **Auto Annotate**：anto annotate images based on yolov5 detector
- [x] **Tracking Annotate**：using tracking method in opencv, annotate video data
- [x] **Magnifing Lens**：helpful when annotating small objects, optional function
- [x] **Data Agument**：data agument
- [x] **Search System**：search details info based on your input
- [x] **Other Tools**：label selecting/rename/counting, fix annotation, video merge/extract, welcome to try
<br>
<br>

🚀(3) **[SAM-Tool](https://github.com/zhouayi/SAM-Tool)**: Customized and Efficient Auto-Annotation based on Segment Anything (SAM) model.
<img src="https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/3-5-3-SAM-Autolabel.gif" width="500">

### 3.6 Autonomous Driving Sensor Suite Calibration Tools

`Sensor suite calibration` is the foundation of any autonomous system and its constituent sensors, and must be performed correctly before achieving sensor fusion. Accurate calibration is crucial for further processing steps, such as sensor fusion and obstacle detection, localization and mapping, and implementation of control algorithms. In addition, sensor fusion is one of the important tasks in autonomous driving applications, which integrates information obtained from multiple sensors to reduce uncertainty compared to using sensors alone.

(1) **[OpenCalib](https://github.com/PJLab-ADG/SensorsCalibration)**: developed and maintained by Shanghai AI Lab.

(2) **[ApolloCalib](https://github.com/ApolloAuto/apollo/tree/master/modules/calibration)**: AD Calibration toolbox launched by Baidu Apollo.

(3) **[AutowareCalib](https://github.com/autowarefoundation/autoware_ai_utilities/tree/master/autoware_camera_lidar_calibrator)**: The calibration tools come with Autoware toolkit.

(4) **[LioxCalib](https://github.com/Livox-SDK/livox_camera_lidar_calibration)**:
This solution provides a method for manually calibrating external parameters between LiDAR and cameras, which has been validated on the Mid-40, Horizon, and Tele-15 series.

### 3.7 AD Visualization Tools

- [Carla-birdeye-view](https://github.com/deepsense-ai/carla-birdeye-view) *An autonomous driving bird's-eye view visualization component that can be inter-connected with Carla*
- [Uber AVS](https://avs.auto/#/) - *AD visualization front-end component`xviz`and `streetscape.gl`*
- [Cruise](https://webviz.io/worldview/#/) -*Cruise.ai open-sourced front-end visualization kit for autonomous driving*

---------------------------------------------
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
