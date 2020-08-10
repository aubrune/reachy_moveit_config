# reachy_moveit2_config
Integration of the Reachy robot in MoveIt 2 for ROS 2

## Install MoveIt

If you're using a ROS distro prior to Noetic, please refer to the [official installing guide](https://moveit.ros.org/install/).
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
