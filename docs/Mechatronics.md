# Mechatronics

## Motors

When researching motors, the first thing I looked was the kind that other hexapod projects used.
Two things were prominent:
1. If a hexapod on the bigger side is what I'm shooting for (4-5kg, 20-30cm leg extension), substantial continuous torque is required, particularly for the [femur joint](https://en.wikipedia.org/wiki/Leg#/media/File:InsectLeg.svg).
The least number of legs touching the ground and supporting the weight is 3, during tripod gaits (without accounting for [unusual ones](https://www.hfsp.org/hfsp-news-events/discovery-bipod-gait-video)), so the continuous torque required is roughly 5(mass) * 9.8(g) / 3 * 0.3(lever length) = 4.9Nm (or roughly 48kg/cm).
Since this is generally [2-4 times smaller](https://www.youtube.com/watch?v=h_SWpU3rmG4&list=PLBRNvqLTPp3t31J8vPxcY-aW_77x5udtQ&index=1) in RC servos, it means having at least [100kg/cm](https://www.trossenrobotics.com/p/mx-106t-dynamixel-robot-servo.aspx) servos like the [Pheonix-MX](http://zentasrobots.com/mx-phoenix-hexapod/), which are very pricey at ~600$.
2. All the other projects found use RC servos, which are only controlled in [position only](https://en.wikipedia.org/wiki/Servo_control).
This is quite limiting since you have no direct control on the torque applied nor on the torque feedback, which are useful for more advanced control (ideas can be anti-skidding or adapting to rough terrain).

All of the research somehow landed towards the amazing [MIT Cheetah 3](https://www.youtube.com/watch?v=QZ1DaQgg3lE) and its [Proprioceptive Actuator Design](https://www.researchgate.net/publication/312558722_Proprioceptive_Actuator_Design_in_the_MIT_Cheetah_Impact_Mitigation_and_High-Bandwidth_Physical_Interaction_for_Dynamic_Legged_Robots).
The idea is to use torque-dense motors with low gear ratios (<10, not >100 like the typical servos) with low inertia limbs to get more direct force feedback directly on the motor.
The motor control loop can compensate directly without complex elastic models of the leg.
It also minimizes impact forces, which are a common cause of failure in rough terrain locomotion.

# References

- [Servo testing](https://www.youtube.com/playlist?list=PL5BftdlCQhcPskezwgKT4Onobk47qVhqG)
- [Compact Gearboxes for Modern Robotics: A Review](https://www.researchgate.net/publication/343655809_Compact_Gearboxes_for_Modern_Robotics_A_Review)
- [Designer’s guide to high-performance motor control for robotics](https://www.electronicproducts.com/designers-guide-to-high-performance-motor-control-for-robotics/)
- [Brushless Inrunner vs Outrunner Motor - RC Motor Basics](https://www.youtube.com/watch?v=m6TW1WZn9CA)
- [CubeMars AK60-6 V1.1](https://store.cubemars.com/goods.php?id=1142), [CubeMars AK70-10](https://store.cubemars.com/goods.php?id=1031)
- [Implementing Torque Control with High-Ratio Gear
Boxes and without Joint-Torque Sensors](https://hal.archives-ouvertes.fr/hal-01136936/file/paper_201403_hal.pdf)
- [The Benefits of Gearboxes — and When to Pick Integrated Gearmotors](https://www.machinedesign.com/motors-drives/article/21833641/the-benefits-of-gearboxes-and-when-to-pick-integrated-gearmotors)
- [Compact Gearboxes for Modern Robotics: A Review](https://www.frontiersin.org/articles/10.3389/frobt.2020.00103/full)
- [AutomataKit BLDC Driver](https://gitlab.cba.mit.edu/jakeread/atkbldcdriver/-/tree/master/)
- [Design for 3D agility and virtual compliance using proprioceptive force control in dynamic legged robots](https://www.ri.cmu.edu/pub_files/2016/8/kaloucheThesis.pdf)
- [Low Cost, High Performance Actuators for Dynamic Robots](https://ceias.nau.edu/capstone/projects/ME/2021/20F09_ExoskeletonActuator/Documents/1057343368-MIT.pdf)
- [Design and Control of a Open-Source, Low Cost, 3D Printed Dynamic Quadruped Robot](https://www.mdpi.com/2076-3417/11/9/3762/htm)
- [Python Motor Driver for Mini Cheetah-type Actuators from T-Motor/CubeMars](https://github.com/dfki-ric-underactuated-lab/mini-cheetah-tmotor-python-can)
- [Ben Katz Blog](https://build-its-inprogress.blogspot.com/)
- [Benjamin Vedder blog](http://vedder.se/)
- [Benjamin Vedder Github](https://github.com/vedderb)