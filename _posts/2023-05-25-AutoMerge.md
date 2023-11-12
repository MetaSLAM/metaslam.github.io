---
layout: post
title: "AutoMerge"
date: 2022-06-20 2:00:01
categories: mapping
description: "AutoMerge"
published: true
image: /img/posts/mapping/automerge/mapping.gif
hide_hero: true
---

## Background and Major Contributions

We present AutoMerge, a LiDAR data processing framework for assembling a large number of map segments into a complete map. Traditional large-scale map merging methods are fragile to incorrect data associations, and are primarily limited to working only offline. AutoMerge utilizes multi-perspective fusion and adaptive loop closure detection for accurate data associations, and it uses incremental merging to assemble large maps from individual trajectory segments given in random order and with no initial estimations. Furthermore, after assembling the segments, AutoMerge performs fine matching and pose-graph optimization to globally smooth the merged map. We demonstrate AutoMerge on both city-scale merging (120km) and campus-scale repeated merging (4.5km x 8). The experiments show that AutoMerge (i) surpasses the second- and third- best methods by 14% and 24% recall in segment retrieval, (ii) achieves comparable 3D mapping accuracy for 120 km large-scale map assembly, (iii) and it is robust to temporally-spaced revisits. To the best of our knowledge, AutoMerge is the first mapping approach that can merge hundreds of kilometers of individual segments without the aid of GPS.

The major contributions of AutoMerge include:

* AutoMerge provides a framework that can merge segments in city-scale environments without requiring initial estimations. Using this framework, we enable multi-agent map merging by being invariant to relative perspective differences and temporal differences.
* Within AutoMerge, we design an adaptive loop-closure detection module, which provides high recall and low false positive place retrievals, resulting in significantly reduced outliers in repeated environments during large-scale merging.
* AutoMerge has the ability to perform incremental map merging for single- and multi-agent systems. This procedure is invariant to the data streaming order from the different agents -- both in the temporal and spatial domain -- and to the revisit times for the same area.
* Extensive evaluation on different large-scale datasets. We demonstrate detailed qualitative and quantitative analysis on the public KITTI dataset, and on our own city-scale and campus-scale datasets, which show that AutoMerge provides accurate map merging performance, and also that it has high generalization for unknown areas.

<figure>
 <img src="/img/posts/mapping/automerge/framework.png" style="width:100%" />
 <figcaption>
AutoMerge supports both offline and online global map merging tasks. In the offline mode, AutoMerge can use the previously-stored sub-maps for direct global data association and map merging. In the online mode, given LiDAR odometry estimates, each agent can extract adaptive place descriptors from local sub-maps and stream them back to the AutoMerge Server. Due to the viewpoint-invariance of these descriptors, AutoMerge can estimate accurate data associations between different segments with less recall. The sub-maps are merged into a global map using a rough global optimization method (GO), and each agent can estimate in parallel their global location through a local optimization (LO) method.
 </figcaption>
</figure>

<figure>
 <img src="/img/posts/mapping/automerge/feature.gif" style="width:45%" />
<img src="/img/posts/mapping/automerge/sequence.gif" style="width:45%" />
 <figcaption>
 Fusion-based 3D feature extraction, and adaptive enhanced Sequence Matching.
 </figcaption>
</figure>

<figure>
 <img src="/img/posts/mapping/automerge/cluster.gif" style="width:45%" />
  <img src="/img/posts/mapping/automerge/mapping.gif" style="width:45%" />
 <figcaption>
Incremental Clustering for Mulait-Agent Mapping and Localization in City of Pittsburgh.
 </figcaption>
</figure>

## Publications

*BibTeX:*
```
@article{yin2022automerge,
  title={Automerge: A framework for map assembling and smoothing in city-scale environments},
  author={Yin, Peng and Lai, Haowen and Zhao, Shiqi and Fu, Ruijie and Cisneros, Ivan and Ge, Ruohai and Zhang, Ji and Choset, Howie and Scherer, Sebastian},
  journal = {IEEE Transactions on Robotics, Conditional Accepted},
  url = {https://arxiv.org/abs/2207.06965},
  video = {https://youtu.be/6sCWeDmQITQ},
  year={2022},
}
```
<!-- ### Contact
* [Peng Yin](https://metaslam.github.io/): (hitmaxtom [at] gmail [dot] com) -->
