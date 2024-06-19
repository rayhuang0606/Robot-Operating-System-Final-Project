#Gazebo Simulation
#Launch Simulation World

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_house.launch

#SLAM Simulation
#Launch Simulation World

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_house.launch

#Run SLAM Node

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

#Run Teleoperation Node

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

#Save Map

rosrun map_server map_saver -f ~/test

#Navigation Simulation
#Launch Simulation World

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_house.launch

#Run Navigation Node

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/test.yaml

#Estimate Initial Pose

#Click the 2D Pose Estimate button in the RViz menu
#Click on the map where the actual robot is located and drag the large green arrow toward the direction where the robot is facing.

#Set Navigation Goal

#Click the 2D Nav Goal button in the RViz menu.
#Click on the map to set the destination of the robot and drag the arrow toward the direction where the robot will be facing.


1093706_Ray Huang_Robot Operating System Final Project
