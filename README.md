# comp3431-ass3-worlds

This ROS2 package contains a sample world for assignment 3.
Follow standard ROS2 package installation procedure for installation.

## Launching the sample house1 world

```
ros2 launch comp3431_ass3_worlds house1.launch.py
```

## Rooms

There are unique QR codes in all rooms that describe the type of room. For house1, the QR codes in each room are as below.

![](images/house1.png)



## Note

The contents of the script `turtlebot3_startup.sh` given in assignment1 is as below:

```
source ~/turtlebot3_ws/install/setup.bash &&
ros2 launch turtlebot3_gazebo turtlebot3_house.launch.py &
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=true
```

Note that the line given to launch the sample house1 world, is a replacement of the second line above.
This means that if you `turtlebot3_startup.sh` after launching the house1 world, you're trying to launch two worlds.
My recommendation would be to add the "setup.bash" line to your bashrc, and add the third cartographer line to a launch file you will write to run all of your nodes in the assignment3.
