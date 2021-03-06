# ROS navigation stack using move_base package
This repository contains a simple implementation of a Global and Local path planner.


## Global path planner
The file **Astar_global_planner.cpp** contains the derived class **Astar** which implementents the base class **BaseGlobalPlanner**. 

The **BaseGlobalPlanner** interface:
- initialize
- makePlan


## Local path planner 
The file **DW_local_planner.cpp** contains the derived class **DynamicWindow** which implementents the base class **BaseLocalPlanner**.

The **BaseLocalPlanner** interface:
- initialize
- computeVelocityCommands
- isGoalReached
- setPlan

Both base classes come from the * nav_core * ROS package and both derived classes need to implement the respective interfaces.

Both classes are exported as plugins and included in the * move_base * navigation stack.

## Installing
To install this project, you have to have ROS installed alongside the following ROS packages:
- stage_ros
- gmapping
- rqt_gui
- rviz
- move_base
- nav_core

You also have to have a Workspace set up, then you can simple clone this project into the ` /src ` folder of your Workspace.

## Building
Simply run catkin_make in your workspace, then source the setup file in the ` /devel ` folder.

## Running
You can run this project by typing ` roslaunch pathplanner CustomCompletePlanner.launch `.

## About
Developed by Muhamed Delalić using ROS Melodic Morenia on Ubuntu 18.04.

## License
This project is licensed under the terms of the MIT license.
