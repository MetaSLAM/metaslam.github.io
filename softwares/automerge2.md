---
title: Showcase
subtitle: An example showcase page
description: An example showcase page to help you easily display your work
layout: page
# showcase: showcase_example
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: /img/posts/automerge2/automerge2.gif
---
## Background and Major Contributions

The visual camera is an attractive device in beyond visual line of sight (B-VLOS) drone operation, since they are low in size, weight, power, and cost, and can provide redundant modality to GPS failures. However, state-of-the-art visual localization algorithms are unable to match visual data that have a significantly different appearance due to illuminations or viewpoints. This paper presents iSimLoc, a condition/viewpoint consistent hierarchical global re-localization approach. The place features of iSimLoc can be utilized to search target images under changing appearances and viewpoints. Additionally, our hierarchical global re-localization module refines in a coarse-to-fine manner, allowing iSimLoc to perform a fast and accurate estimation. We evaluate our method on one dataset with appearance variations and one dataset that focuses on demonstrating large-scale matching over a long flight in complicated environments. On our two datasets, iSimLoc achieves 88.7% and 83.8% successful retrieval rates with 1.5s inferencing time, compared to 45.8% and 39.7% using the next best method. These results demonstrate robust localization in a range of environments.

The major contributions of iSimLoc include:

* **We developped a novel long-term (variant illumiations) and large-scale (150km) UAV navigation method.**
* **The proposed method can achieve accurate  without been there .**
* **The proposed method only requires 5~10% original data for model training**
* **The proposed method can provide large-scale re-localization under challenge terrains.**

<figure>
 <img src="/img/posts/isimloc/framework.png" style="width:100%" />
 <figcaption>
For high and low altitudes, iSimLoc extracts a condition-(illumination) and viewpoint-invariant place descriptor. Only the descriptor needs to be stored and matched. Larger field of views help iSimLoc to provide an initial guess, while narrower field of view perspectives provide rich local geometry features for accurate localization. iSimLoc matches hierarchically, which enables us to balance search efficiency and accuracy.
 </figcaption>
</figure>

## Publications

*BibTeX:*
```
@article{yin2022isimloc,
  title={iSimLoc: Visual Global Localization for Previously Unseen Environments with Simulated Images},
  author={Yin, Peng and Cisneros, Ivan and Zhang, Ji and Choset, Howie and Scherer, Sebastian},
  journal = {IEEE Transactions on Robotics, Conditional Accepted},
  url = {https://arxiv.org/abs/2209.06376},
  year={2022},
}
```
### Contact
* [Peng Yin](https://metaslam.github.io/): (hitmaxtom [at] gmail [dot] com)
