# task-5-AI



First we visit turtlebot3 website https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup     to install TurtleBot3 using the quick start quide to download.


Installation steps:

1#Install ROS on Remote PC:-
$sudo apt update
$sudo apt upgrade
$wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools
$chmod 755 ./install_ros_noetic.sh 
$bash ./install_ros_noetic.sh


2#Install Dependent ROS Packages:-

sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy
ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc
ros-noetic-rgbd-launch ros-noetic-rosserial-arduino
ros-noetic-rosserial-python ros-noetic-rosserial-client
ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server
ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro
ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz
ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers



3#Install TurtleBot3 Packages:-

 sudo apt install ros-noetic-dynamixel-sdk
 sudo apt install ros-noetic-turtlebot3-msgs
 sudo apt install ros-noetic-turtlebot3
 
 4#Simulation
 Gazebo simulation
 The TurtleBot3 Simulation Package has needs that must be met, including the turtlebot3 and turtlebot3 msgs packages.
 
 cd ~/catkin_ws/src/ 
 git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git 
 cd ~/catkin_ws && catkin_make

There are three simulation environments ready for TurtleBot3 to start Simulation World. To launch Gazebo, we can choose one of these environments.
 1-Burger
 2-waffle
 3-House
 export TURTLEBOT3_MODEL=waffle
 roslaunch turtlebot3_gazebo turtlebot3_world.launch
 roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
 
 5#SLAM simulation
 Launch Simulation World

export TURTLEBOT3_MODEL=waffle 
roslaunch turtlebot3_gazebo turtlebot3_world.launch

Run SLAM Node

export TURTLEBOT3_MODEL=waffle 
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

Run Teleoperation Node

export TURTLEBOT3_MODEL=waffle
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
source ~/.bashrc

Image:
![image](https://user-images.githubusercontent.com/103290641/185782599-12dfe277-ce58-496c-9cc1-f37c3103f7c4.png)

