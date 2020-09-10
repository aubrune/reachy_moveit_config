# Reachy MoveIt config
Integration of the Reachy robot in MoveIt for ROS 1

![Reachy in RViz ROS Noetic](https://raw.githubusercontent.com/aubrune/reachy_moveit_config/master/doc/img/moveit.png)

## Getting started
Make sure you have installed [ROS 1](http://wiki.ros.org/noetic/Installation), [MoveIt](https://moveit.ros.org/) (see below), and [Reachy Description](https://github.com/aubrune/reachy_description) first. Then launch the regular demo launchfile:
```
roslaunch reachy_moveit_config demo.launch
```

Pickup a group in the **Query Planning Group** from the **Motion Planning** panel (right arm, left arm or head) and move the blue ball appearing at the tip of the end effector to some goal pose. Then click **Plan and Execute** to plan a trajectory with obstacle avoidance and run it with fake trajectory controllers.

## Install MoveIt

If you are using a ROS distro prior to Noetic, please refer to the [official installing guide](https://moveit.ros.org/install/).
As of july 2020, MoveIt is not available as binaris for ROS 1 Noetic, so here's a procedure to compile it:
```
cd ~/ros_ws/src
git clone https://github.com/ros-planning/moveit.git -b noetic-devel
git clone https://github.com/ros-planning/moveit_resources.git
git clone https://github.com/OctoMap/octomap_msgs.git -b melodic-devel
git clone https://github.com/PickNikRobotics/rosparam_shortcuts.git -b noetic-devel
cd ~/ros_ws
rosdep install --rosdistro noetic --from-paths src --ignore-src -r -y
catkin_make
```

