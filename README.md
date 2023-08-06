# Telegabot ROS Package
This repository contains a collection of ROS packages for the Telegabot robot. Telegabot is a mobile robot designed for 2D navigation and control in a simulated environment. The packages provided here include configurations, descriptions, control, and launch files required to run the robot in ROS.

## Package Structure
The repository is organized into several ROS packages:

### telegabot_2dnav
This package provides the necessary configurations for the 2D navigation of the Telegabot robot. It includes configuration files for costmaps, move_base parameters, and launch files to start the navigation stack. The maps directory contains the map file used for navigation.

### telegabot_config
This package contains configurations related to the Telegabot simulation and software launch. It includes launch files for starting the Gazebo simulation and the robot's software components. Additionally, it provides an RViz configuration for visualization.

### telegabot_control
The telegabot_control package contains the configuration file for controlling the robot. It provides the necessary parameters for the robot's control and a launch file to start the control node.

### telegabot_description
This package contains the URDF description of the Telegabot robot. It includes meshes for the robot's base link, wheels, and LIDAR sensor. The URDF description is used for visualization and simulation.

### telegabot_gazebo
The telegabot_gazebo package contains launch files for running the robot in the Gazebo simulator. The worlds directory includes the Gazebo world file in which the robot operates.

## Installation and Usage
To use the Telegabot ROS packages, follow these steps:

Clone the repository into your ROS workspace (e.g., catkin_ws/src).
'''bash
git clone https://github.com/AlexanderRex/telegabot.git catkin_ws/src

Build the packages using catkin.
'''bash

cd catkin_ws
catkin_make

Source the setup file.
'''bash
source devel/setup.bash

Launch the desired components using the provided launch files. For example, to launch the 2D navigation stack and control:

'''bash
roslaunch telegabot_config telegabot_software.launch
roslaunch telegabot_2dnav telegabot_move_base.launch
roslaunch telegabot_control telegabot_control.launch

To run the simulation in Gazebo:
'''bash

roslaunch telegabot_gazebo telegabot_world.launch
