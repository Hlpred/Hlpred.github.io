---
title: Distributed GNC for multi-satellite Systems
subtitle: Research Project for the Air Force Research Laboratory (AFRL)
image: assets\img\portfolio\Performance_Comparison.png
alt: Keep Exploring

caption:
  title: Distributed Satellite GNC
  subtitle: Research Project
  thumbnail: assets\img\portfolio\satellite_thumbnail.jpg
---

In order for close proximity satellites to safely perform their missions, the relative states of all satellites and pieces of debris must be well understood. This presents a problem for ground based tracking and orbit determination since it may not be practical to achieve the required accuracy. Using space based sensors allows for more accurate relative state estimates, especially if multiple satellites are allowed to communicate. This project focused on the case where several communicating satellites each need to maintain a local catalog of communicating and non-communicating objects using angles-only limited field of view (FOV) measurements. However, this introduces the problem of efficiently scheduling and coordinating observations among the agents. A decentralized task allocation algorithm was developed to address this problem. Its performance was quanitified in terms of fuel usage and overall catalog uncertainty via numerical simulation. It was found that the new method significantly outperforms the uncertainty-fuel Pareto frontier formed by current approaches.

The algoirhitm developed for this project utilizes the [CBBA algorithm](https://ieeexplore.ieee.org/document/5072249) to coordinate decentralized task allocation between agents, makes use of a new scoring function to determine the observation quality of a given target, and uses the rate of decrease of this score to inform target switching. Previous work looked at using a hysteresis-based appraoch to initiate target switches. The figure above plots the performance of algorihtims on a total catalog uncertianty (vertical axis) versus fuel (horizontal axis) scatter plot. As expected, varying the hysteresis duration forms a clear Pareto frontier. The new approach falls well below this line meaning that it represents a more capable algorihim in terms of these metrics. A research paper was written that explains this project and its findings in more detail. Its abstract has been submitted to the [AAS GNC Conference](https://aas-rocky-mountain-section.org).