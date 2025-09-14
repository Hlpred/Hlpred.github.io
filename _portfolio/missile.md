---
caption: #what displays in the portfolio grid:
  title: Missile GNC Simulation
  subtitle: Personal Project
  thumbnail: assets\img\portfolio\missile_thumbnail.PNG
  
#what displays when the item is clicked:
title: Missile GNC Simulation
type: video
video_url: https://www.youtube.com/embed/X1CDIxr9Qjc?si=G-sgGpwjcZO5V3jm
subtitle: Personal project in MATLAB / Simulink

---
The goal of this project was to design guidance, navigation, and control algorihtims that could be used to hit a manuvering target with a missle. The missile in question has constant thrust but is able to send control torque commands at each time step. It has acess to gyroscope, target direction, and target closing velcoity sensor data. The target itself is constantly manuvering according to slow sinusodial accelerations, but the missile does not have acess to this information. It is only able observe and react to the result of these manuvers.

The guidance system uses Proportional Navigation to generate a desired acceleration perpendicular to the line of sight to the target. Its magnitude is proportional to the closing velocity and the rate of change of the line of sight direction. With this desired acceleration, the program calculates the orientation of the rocket that would lead to this acceleration. This desired attitude can now be handed off to the attitude control system. It works by finding the Euler angles that correspond to the difference between the current and the desired orientations. From here, these "Error Euler Angles" are sent to a PD controller that applies control torques in the appropritate directions. State estimation is handled by applying dead reckoning to the gyroscope data.

The algorithims were tested under a variety of missile initial conditions, external disturbances, and sensor noise intensities. It was found the current system is sensitive to sensor nosie in the target direction measurmenets. This is partially because the derivative of a noisy signal must be taken to find the rate of change of the line of sight. This was mitigated by using several low pass filters. A future iteration of this project could incoporate a Kalman filter for more accurate state estimation of both the missile and target. 

GitHub Repository: [Link](https://github.com/Hlpred/Missile-Guidance)