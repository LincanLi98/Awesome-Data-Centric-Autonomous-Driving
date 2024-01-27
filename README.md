# Awesome Data-Centric Autonomous Driving [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

**This is the official repository of our survey paper**:[Data-Centric Evolution in Autonomous Driving: A Comprehensive Survey of Big Data System, Data Mining, and Closed-Loop Technologies](https://arxiv.org/abs/2401.12888)

## Category
- [1. Motivation and Background of Data-Driven Autonomous Driving(background)](#1-Motivation-and-Background-of-Data-Driven-Autonomous-Driving)
  - [1.1 Performance Upper Bound of Autonomous Driving Algorithms](#11-Performance-Upper-Bound-of-Autonomous-Driving-Algorithms)
  - [1.2 Reasons of Data-Driven Autonomous Driving](#12-Reasons-of-Data-Driven-Autonomous-Driving)
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

Most of the collected AD big data comes from normal driving scenarios, of which we already have huge amount of similar samples in the database. But the ambition of Data-Centric Autonomous Driving lies in the **automatic observing of long-tail distribution challenging scenarios**, and the **self-evolution of AD intelligent algorithms/models**.

![image](https://github.com/LincanLi98/Awesome-Data-Centric-Autonomous-Driving/blob/main/img_resource/1-1_Long_Tail_Distribution.png){width=1000px height=412px}

### Acknowledgements to Our Research Work
Thanks for the appreciation of our research. If you use part of the content of our research, please cite our work as follows:
```
@misc{li2024datacentric,
      title={Data-Centric Evolution in Autonomous Driving: A Comprehensive Survey of Big Data System, Data Mining, and Closed-Loop Technologies}, 
      author={Lincan Li and Wei Shao and Wei Dong and Yijun Tian and Kaixiang Yang and Wenjie Zhang},
      year={2024},
      eprint={2401.12888},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}
```
