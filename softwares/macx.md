---
title: MACX
subtitle: Multi-Agent Cooperative Exploration with Unknown Initial Position
description: Multi-Agent Cooperative Exploration with Unknown Initial Position
layout: page
# showcase: showcase_example
show_sidebar: false
hide_footer: false
hero_height: is-large
hero_image: /img/posts/macx/macx.gif
---
## Background and Major Contributions

Multi-agent exploration of a bounded 3D environment with unknown initial positions of agents is a challenging problem. It requires quickly exploring the environments as well as robustly merging the sub-maps built by each agent. We take the view that the existing approaches are either aggressive or conservative: Aggressive strategies directly merge sub-maps when there seems to be overlap between two sub-maps, which can lead to incorrect merging due to the false-positive detection of overlap and is thus not robust. Conservative strategies direct one agent to revisit excessive amount of the history trajectory of another agent for verification before merging, which can lower the exploration efficiency due to the repeated exploration of the same area. To intelligently balance the robustness of sub-map merging and exploration efficiency, we develop a new approach for lidar-based multi-agent exploration, which can direct one agent to repeat another agent's trajectory in an adaptive manner based on the quality indicator of the sub-map merging process. Additionally, our approach extends the recent single-agent hierarchical exploration strategy to multiple agents in a cooperative manner by planning for agents with merged sub-maps together to further improve the exploration efficiency. Our numerical results show that our approach is xxx more efficient than the baselines on average while maintaining the robustness of sub-map merging.

The major contributions of MACX include:

* **We developped a novel large-scale multi-agent exploration method.**
* **The proposed method don't relay on initial information of other agents.**
* **The proposed method can incrementally explore unknown environments.**
* **The proposed method can achievely increase overlaps between agents to improve mapping.**

<figure>
 <img src="/img/posts/macx/active1.png" style="width:45%" />
 <img src="/img/posts/macx/active2.png" style="width:45%" />
 <figcaption>
Given the merged map and relative pose, the exploration path will be planned hierarchically on each sub-map. The local subspace planner will plan a detailed path in its local planning subspace, which covers all the uncovered surfaces in the local space. The global planner model the coordination of the multi-agent system as a multi-Traveling salesmen problem. The final exploration path will be produced by concatenating the local and global paths.
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
