# iqr_kobuki_robot
The mobile robot kobuki with TX2, velodyne16, pan_tilt, ZED, kinectV2, jy901
## Overview
The package is mainly used for the driving of kuboki mobile robot, and other sensors. Demo for navigation based on laser, and other uses of depth camera.
## Environment
Ubuntu18.04\
ROS-melodic
## quick start
### install
```bash
git clone https://github.com/I-Quotient-Robotics/iqr_kobuki_robot.git
cd iqr_kobuki_robot
rosdep install --from-paths ./ -i -y --rosdistro kinetic
```
### driver
```bash
cd workspace
catkin_make
source /devel/setup.bash
roslaunch iqr_kobuki_bringup iqr_kobuki_bringup.launch
```
### map
```bash
roslaunch iqr_kobuki_navigation gmapping.launch
rosrun map_server map_saver -f map # save map
```
### navigation demo
```bash
roslaunch iqr_kobuki_navigation navigation.launch
```
