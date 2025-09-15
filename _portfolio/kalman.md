---
title: Extended Kalman Filter
subtitle: Personal Project in MATLAB / Simulink
image: assets\img\portfolio\Kalman.png
alt: Shirts on a hanger

caption:
  title: Extended Kalman Filter
  subtitle: Personal Project
  thumbnail: assets\img\portfolio\Kalman.png
---

The goal of this project was to design a state estimation algorithm for a rocket with inertial and angles-only optical sensors. In other words, how can unit vectors corresponding to the locations of fixed points on the ground be effectively incorporated into state estimates. One of the challenges with this problem is that the attitude dynamics and camera measurements are nonlinear. The attitude dynamics could be linearized around the rocket up position, however, there is no such simplification for the camera measurements since it is assumed that the rocket has the potential to move significantly along all three axes. Therefore, the extended Kalman Filter (or EKF) was chosen due to its ability to handle nonlinear system dynamics and measurement models. The EKF works by using taking the Jacobian of the system dynamics and measurement models at every time step in order to find matrices that can be used in the original Kalman Filter equations. Essentially, this linearizes the system about its current state. Since the state vector chosen for this project is 21 dimensional, the nonlinear equations were written as symbolic functions so that MATLAB could compute their Jacobians.

Another challenge associated with this project was that the sensor measurements available might not be the same at every time step (either because images can not be taken that quickly or because it would be impractical to process that many). Additionally, the set of points that are recognized by the computer vision (CV) system may change from one time step to the next even if the same points are still visible to the cameras. All of this means that the EKF needs to dynamically adjust the size of its matrices to fit the dimensions of the measurement data. In practice, this means computing the full matrices and ignoring specific rows and columns corresponding to the measurements that are not currently available.

The EKF algorithm designed for this project was compared to dead reckoning of the inertial measurements for several different rocket trajectories and sensor noise / bias values. It was found that an EKF is most beneficial when the inertial measurements have large uncertainties. This is demonstrated by the figure above that shows a large difference (note the scale factor on the second plot) in the Euler Angle errors when the inertial measurements have significant noise and bias. However, an EKF may be difficult to implement in practice due to its high computational requirements and the fact that the noise values (especially the process noise) values are often not well understood for real world systems.

GitHub Repository: [Link](https://github.com/Hlpred/Kalman/tree/main)