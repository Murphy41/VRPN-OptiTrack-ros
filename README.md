# vrpn-client-ros
A guide for setting up the VRPN client in ROS for receiving data from the Optitrack.

# Optitrack Server Side Setup
Please refer to [Optitrack Motive VRPN Streaming Setup and Configure Guidance]().

# VRPN Client Side Setup
The Virtual-Reality Peripheral Network (VRPN) is a set of classes within a library and a set of servers that are designed to implement a network-transparent interface between application programs and the set of physical devices (tracker, etc.) used in a virtual-reality (VR) system. In this repo, we'll only focus on the Optitrack device.

## Submodule in this repo
[vrpn_client_ros](https://github.com/Murphy41/vrpn_client_ros)

[vrpn_catkin](https://github.com/ethz-asl/vrpn_catkin)

[catkin_simple](https://github.com/catkin/catkin_simple)

## Installation
In the src folder in your workspace run the following command:

git clone

Then, navigate back to the workspace root path, run:

catkin_make

## Configuration

A sample launch file is given in src/VRPN-OptiTrack-ros/vrpn_client_ros/launch path. The rosparam in it can be configured based on your needs. In the common case, to run this sample, just check the server ip address and port in the launch file. You can either change the default ip in the launch file directly or state it when use roslaunch.

## Test

To test the sample launch file, simply use the following code, and replace the following ip address with the ip address of your OptiTrack server.

roslaunch vrpn_client_ros sample.launch server:=128.130.39.61 & rosrun rviz rviz


# Acknowledgement
The vrpn_client_ros noetic version is forked from [usrl-uofsc/vrpn_client_ros](https://github.com/usrl-uofsc/vrpn_client_ros) which is developed based on [ros-drivers/vrpn_client_ros](https://github.com/ros-drivers/vrpn_client_ros)