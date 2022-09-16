---
title: ALITA
subtitle: A Large-scale Incremental Dataset for Long-term Autonomy
description: A Large-scale Incremental Dataset for Long-term Autonomy
layout: page
# showcase: showcase_example
show_sidebar: false
hide_footer: false
# hero_height: is-large
# hero_image: /img/posts/alita/urban.png
---

## Background and Major Contributions
For long-term autonomy, most place recognition methods are mainly evaluated on simplified scenarios or simulated datasets, which cannot provide solid evidence to evaluate the readiness for current Simultaneous Localization and Mapping (SLAM).This paper presents a long-term place recognition dataset for use in mobile localization under large-scale dynamic environments.This dataset includes a campus-scale track and a city-scale track.The campus track focuses on the long-term property and is recorded with a LiDAR device and an omnidirectional camera on 10 trajectories. Each trajectory is repeatedly recorded 8 times under variant illumination conditions. The city track focuses on the large-scale property and is recorded only with the LiDAR device on 120km trajectory, which contains open streets, residential areas, natural terrains, etc. They include 200 hours of raw data of all kinds of scenarios within urban environments. The ground truth position for both tracks is provided on each trajectory, obtained from the Global Position System with an additional General ICP-based point cloud refinement. To simplify the evaluation procedure, we also provide the Python-API with a set of place recognition metrics proposed to quickly load our dataset and evaluate the recognition performance against different methods.This dataset targets finding methods with high place recognition accuracy and robustness and providing real robotic systems with long-term autonomy. We provide both the dataset and tools at[ALITA](https://github.com/MetaSLAM/ALITA)

## The major properties of ALITA

Our datasets contain two tracks: 
* Urban dataset, which records LiDAR data inputs in a city-scale urban-like area for 50 segments and 120km trajectory in total.
* Campus dataset, recorded under a campus-scale environment, where we gathered the omnidirectional visual inputs and LiDAR inputs on 10 different trajectories for 8 repeated times, under different illuminations and viewpoints; this dataset targets long-term localization challenge.

Below figures give a better visualization of its scale, and Table.1 shows the comparison of different datasets. Most datasets are targeted at short-term, fixed conditions or viewpoints place recognition tasks, so it is hard to evaluate the localization performance in real-world long-term, large-scale applications. Compared to existing datasets, our **Urban** dataset covers variant 3D scenarios for comprehensive 3D place recognition evaluation and multi-session SLAM. And our **Campus** dataset repeatedly covers diverse campus areas with dynamic objects, illumination, and viewpoint differences, which is suitable to evaluate long-term re-localization or incremental learning ability.

<figure>
 <img src="/img/posts/alita/alita_city.gif" style="width:49%" />
 <img src="/img/posts/alita/alita_campus.gif" style="width:49%" />
 <figcaption>
Datasets for City of Pittsburgh and Campus of Carnegie Mellon University 
 </figcaption>
</figure>

<figure>
 <img src="/img/posts/alita/data_compare.png" style="width:70%" />
 <figcaption>
Table.1. Property comparsion with other datasets.
 </figcaption>
</figure>

## Publications

*BibTeX:*
```
@article{yin2022alita,
  title={ALITA: A Large-scale Incremental Dataset for Long-term Autonomy},
  author={Yin, Peng and Zhao, Shiqi and Ge, Ruohai and Cisneros, Ivan and Fu, Ruijie and Zhang, Ji and Choset, Howie and Scherer, Sebastian},
  journal={arXiv preprint arXiv:2205.10737},
  year={2022},
  url={https://github.com/MetaSLAM/ALITA}
}
```
### Contact
* [Peng Yin](https://metaslam.github.io/): (hitmaxtom [at] gmail [dot] com)
