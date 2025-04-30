# Vacuum Cleaner Bot
### Autonomous Robotics open ended project
---
### Install the following first
```bash
sudo apt-get install ros-noetic-move-base ros-noetic-turtlebot3-bringup ros-noetic-turtlebot3-navigation ros-noetic-explore-lite
```

### Next steps:
Download this repo and cd into the catkin_ws 

### Setup workspace
```bash
catkin_make
```
```bash
source setup.sh
source setup.bash
```
### Runing
```bash
export TURTLEBOT3_MODEL=waffle_pi
```

Launch gazebo with cleaner_bot
```bash
roslaunch cleaner_bot gazebo.launch
```

explore explore.launch 
```bash
roslaunch cleaner_bot explore.launch
```

Save the scanned map with following command:    
```bash
rosrun map_server map_saver --occ 90 --free 10 -f ~/catkin_ws/src/cleaner_bot/map/<YOUR_MAP> map:=/map
```

Start performing cleaning by closing the exploration node and running the following:

```bash
roslaunch cleaner_bot <YOUR SCANNED MAP>.launch 
```


Sources: 
1. [Github: Tofigh-Tevfik/cleaner_bot](https://github.com/Tofigh-Tevfik/cleaner_bot)
2. [Github: peterWon/CleaningRobot](https://github.com/peterWon/CleaningRobot)
3. [Github: Intenzo21/ROS-vacuum-cleaner](https://github.com/Intenzo21/ROS-vacuum-cleaner)
4. [Medium: Robot Vacuum Cleaner Part 3/3](https://medium.com/cse-468-568-robotic-algorithms/robot-vacuum-cleaner-part-3-3-2bc317cf17db)

 

