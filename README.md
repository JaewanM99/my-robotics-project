ROS2 Line-Following Robot with Pure Pursuit Steering
Description:
A ROS2-based line-following robot using computer vision and Pure Pursuit steering for smooth navigation. Detects tape paths via adaptive thresholding, calculates curvature, and sends serial commands to control motion in real time.

Features
- Real-time image processing using ROS2
- Adaptive thresholding for tape detection
- Pure Pursuit algorithm for path tracking
- Multi-row sampling for better path prediction
- Serial communication for motor control

Tech Stack
-Language: C++
-Framework: ROS2
-Hardware: Camera module, microcontroller (e.g., Arduino or Raspberry Pi), motor driver
-Algorithms: Pure Pursuit steering, adaptive thresholding

Installation & Setup
1. Clone the Repository
   git clone https://github.com/JaewanM99/ros2-line-following-robot.git
   cd ros2-line-following-robot
2. Build the ROS2 Package
   colcon build
   source install/setup.bash
3. Run the Node
   ros2 run line_tracker line_tracker_node
   
How It Works
1.Captures frames from the camera.
2.Converts image to grayscale and applies adaptive thresholding.
3.Detects tape center and calculates lateral offset.
4.Applies Pure Pursuit formula to compute curvature.
5.Sends steering commands via serial to control the robot.

---

## Code Overview
This repository contains the main algorithm files:
- **src/line_tracker.cpp** – Implements line detection and Pure Pursuit steering.
- (Optional) **src/multi_row_version.cpp** – Enhanced version with multiple rows for better path prediction.

> Note: This is the core logic only and does not include full ROS2 package configuration.

---

##  Images 
Here is the robot in action:

<p align="center">
  <img src="images/robot.jpg" width="400">
</p>

<p align="center">
  <img src="images/robot_1.jpg" width="400">
</p>



###  Video Demo
[▶ Watch on YouTube]()

---

## License
MIT License. Feel free to use and modify.

---
