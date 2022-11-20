# Other works

There is a ton of different hexapods robots, but I'm concentrating on spider-like, 3 or 4 DoF per leg, recent (<10 years old) ones.

## Hexa

<img src="https://robots.ieee.org/robots/hexa/Photos/SD/hexa-photo1-full.jpg" height="300" />

[Docs](https://documentation.vincross.com/index.html), [Video](https://www.youtube.com/watch?v=5OQrAyfnBBo)
- medium-small, plastic structure, lovely design
- 3-DoF legs with adaptable movement but not very fluent
- camera, probably CPU only
- includes a simulator
- only limited parts are open-sourced, many info not available

## Jethexa

<img src="https://www.hiwonder.it/wp-content/uploads/2022/08/Jethexa-3-600x600.jpeg" height="300" />

[Info](https://www.hiwonder.it/prodotti/jethexa/), [Video](https://www.youtube.com/watch?v=S0lCqG-T-tA)
- medium, aluminum structure
- 3-DoF legs with adaptable movement but not very fluent
- 3.5Nm torque servos, 2.5kg robot
- depth camera (Realsense), LiDAR (YDLIDAR G4), Jetson nano
- claimed open source (many ROS features), but could not find it

## Make your pet

<img src="https://i.all3dp.com/workers/images/fit=cover,w=1284,h=722,gravity=0.5x0.5,format=auto/wp-content/uploads/2022/10/17163451/hexapodnewsstory.jpg" height="300" />

[Repo](https://github.com/MakeYourPet/hexapod), [Video](https://www.youtube.com/watch?v=6T8NDrmyjwc)
- medium, 3d printed structure
- 3-DoF legs with touch sensors, quite fluent
- no perception, android logic running on cellphone
- open source design, did not find SW code but the author is open for sharing
- nice tutorials

## MX-Phoenix

<img src="https://www.digitaltrends.com/wp-content/uploads/2017/04/P1074123.jpg?fit=720%2C480&p=1" height="300" />

[Info](http://zentasrobots.com/mx-phoenix-hexapod/), [Video](https://www.youtube.com/watch?v=mcw_0cIyr9Y)
- large, 3d printed structure
- 3-DoF legs, very fluent, large steps
- 12x10Nm, 6x8Nm torque servos (worth 8k$!), 4.7kg robot
- no perception
- no open source material

## WidowX MK-IV

<img src="https://www.trossenrobotics.com/Shared/Images/Product/WidowX-Hexapod-MK-IV/Front_and_Center_Square.png" height="300" />

[Info](https://www.trossenrobotics.com/widowx-hexapod-mk4.aspx), [Repo](https://github.com/Interbotix/interbotix_ros_crawlers/tree/main/interbotix_ros_xshexapods), [Video](https://www.youtube.com/watch?v=0fMXJBiTIVo)
- medium, 3d printed shell on aluminum structure
- 3-DoF legs, not very fluent
- 3.8Nm servos (the most powerful version)
- no perception, Raspberry Pi 4 Model B
- well documented SW

## SmallpTsai Hexapod

<img src="https://pbs.twimg.com/profile_images/1113669143977324545/vwCYQ-fR_400x400.png" height="300" />

[Repo](https://github.com/SmallpTsai/hexapod-v2-7697), [Video](https://www.youtube.com/watch?v=To2Y6Mhu-CE)
- small, 3d printed
- 3-DoF legs, quite fluent
- 0.35Nm servos
- no perception, LinkIt-7697 board
- very well documented