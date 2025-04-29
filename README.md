# Vacuum Cleaner Bot
### Autonomous Robotics open ended project
---
### Install the following first
```bash
sudo apt-get install ros-noetic-move-base ros-noetic-turtlebot3-bringup ros-noetic-turtlebot3-navigation ros-noetic-explore-lite
```

### Next steps:
Download this repo and cd into the catkin_ws 

### Runing
```bash
catkin_make
```
```bash
export TURTLEBOT3_MODEL=waffle_pi
```
```bash
roslaunch cleaner_bot gazebo.launch
```
Save your map with following command:

```bash
rosrun map_server map_saver --occ 90 --free 10 -f ~/catkin_ws/src/cleaner_bot/map/<YOUR_MAP> map:=/map
```

Start performing cleaning by closing the exploration node and running the following:

```bash
roslaunch cleaner_bot do_cleaning.launch
```


