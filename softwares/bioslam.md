---
title: BioSLAM
subtitle: An example showcase page
description: An example showcase page to help you easily display your work
layout: page
# showcase: showcase_example
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: /img/posts/bioslam/bioslam.gif
---

## Background and Major Contributions
We present BioSLAM, a lifelong SLAM framework for learning various new appearances incrementally and maintaining accurate place recognition for previously visited areas. Unlike humans, artificial neural networks suffer from catastrophic forgetting and may forget the previously visited areas when trained with new arrivals. For humans, researchers discover that there exists a memory replay mechanism in the brain to keep the neuron active for previous events. Inspired by this discovery, BioSLAM designs a gated generative replay to control the robot's learning behavior based on the feedback rewards. Specifically, BioSLAM provides a novel dual-memory mechanism for maintenance: 1) a dynamic memory to efficiently learn new observations and 2) a static memory to balance new-old knowledge. When combined with a visual-/LiDAR- based SLAM system, the complete processing pipeline can help the agent incrementally update the place recognition ability, robust to the increasing complexity of long-term place recognition.

We demonstrate BioSLAM in two incremental SLAM scenarios. In the first scenario, a LiDAR-based agent continuously travels through a city-scale environment with a 120km trajectory and encounters different types of 3D geometries (open streets, residential areas, commercial buildings). We show that BioSLAM can incrementally update the agent's place recognition ability and outperforming the state-of-the-art incremental approach, Generative Replay, by 24%. In the second scenario, a LiDAR-vision-based agent repeatedly travels through a campus-scale area on a 4.5km trajectory.BioSLAM can guarantee the place recognition accuracy to outperform 15% over the state-of-the-art approaches under different appearances. To our knowledge, BioSLAM is the first memory-enhanced lifelong SLAM system to help incremental place recognition in long-term navigation tasks.


The major contributions of iSimLoc include:

* BioSLAM provides a systematic framework to learn about ever-changing environments without interruption. Using this framework, we enable incremental place feature learning in the long-term autonomy.
* Within BioSLAM, we develop a dual-memory module, which includes 1) a dynamic memory zone with high-frequency updates for fast adaptation of new patterns and 2) a static memory zone with low-frequency updates for long-term memory retention.
* BioSLAM can perform non-stop online learning for new environments and provide lifelong re-localization ability for previously visited areas even under changing environmental conditions.Furtherly, the module design of BioSLAM makes it possible to be combined with arbitrary place descriptor learning modules.
* We developed extensive lifelong localization datasets and relative metrics to evaluate the lifelong localization performance and demonstrate a detailed analysis of adaptation efficiency and long-term memory retention ability.

<figure>
 <img src="/img/posts/bioslam/bio_idea.gif" style="width:45%" />
 <img src="/img/posts/bioslam/robo_idea.gif" style="width:45%" />
 <figcaption>
For high and low altitudes, iSimLoc extracts a condition-(illumination) and viewpoint-invariant place descriptor. Only the descriptor needs to be stored and matched. Larger field of views help iSimLoc to provide an initial guess, while narrower field of view perspectives provide rich local geometry features for accurate localization. iSimLoc matches hierarchically, which enables us to balance search efficiency and accuracy.
 </figcaption>
</figure>

## Publications

*BibTeX:*
```
@article{yin2022bioslam,
  title={BioSLAM: A Bio-inspired Lifelong Memory System for General Place Recognition},
  author={Yin, Peng and Abuduweili, Abulikemu and Zhao, Shiqi and Liu, Changliu and Scherer, Sebastian},
  journal={IEEE Transactions on Robotics, Conditional Accepted},
  url={https://arxiv.org/abs/2208.14543},
  video={https://youtu.be/PPOmyz2UVIw},
  year={2022},
}
```
### Contact
* [Peng Yin](https://metaslam.github.io/): (hitmaxtom [at] gmail [dot] com)
