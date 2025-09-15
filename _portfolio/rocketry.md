---
title: Prometheus Testing Campaign
subtitle: Club Project
type: video
video_url: https://www.youtube.com/embed/8p5pTC6pLIs?si=_ee0KE-uKKMjNg5f

caption:
  title: Prometheus Testing Campaign
  subtitle: Club Project
  thumbnail: assets\img\portfolio\stability_stand_thumbnail.png
---

Propulsive Landing was an engineering team at UConn that aimed to build a thrust vector controlled (TVC) model rocket capable of autonomous launch and landing. As team lead of Propulsive Landing last year, I planned out a series of tests that our rocket (Prometheus) needed to complete in order to achieve this goal. For example, the stability stand test. This is where the rocket is attached to a two axis gimbal that allows it to rotate. From here, the rocket motor can be lit and the control system will attempt to use the TVC to bring the rocket to a vertical orientation. A successful stability stand test is a crucial milestone because it demonstrates the functionality of all rocket systems needed for stable flight. Prometheus' first stability stand test involved the motor igniting several seconds late, no data written to the flight computer, and the stability stand tipping over. A number of modifications were made to the vehicle after this test including flight computer triggered ignition, smaller E class rocket motors, and through software in the loop testing of Prometheus' flight software. These fixes lead to a much more successful stability stand test in May 2025 where Prometheus was close to vertical at motor cutoff. However, a number of new issues were noted such as play in the TVC mechanism, control weights that were not aggressive enough, and the spin caused by ejection at the end of the ascent burn. For the first launch and land test, all of these issues were addressed along with modifications to the rocket's center of mass to account for its new landing legs. Prometheus' first flight demonstrated controlled ascent, however, the igniters for the two stages were swapped meaning that the descent motor performed the ascent and ejected the descent motor in the process.

In addition to working through all of these issues with the team, I was responsible for simulating and modifying the navigation and control algorithms in our flight software. This often involved retune our controller with monte carlo simulations to ensure that the current control weights could meet our mission objectives. The control system itself was a gain scheduled LQR controller that would change the control matrix K as the expected thrust of the motor changed. Additionally, I worked closely with our software team to develop a version of the simulation that could directly interface with our flight software code. This gave us much more confidence that we would not be encountering bugs for the first time during a real world test. 

GitHub: [Propulsive Landing (now UConn Rocketry)](https://github.com/UConn-Rocketry)