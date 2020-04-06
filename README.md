# racecar_ROSpackage_melodic
# Here are the steps required to run the racecar gazebo model. 

1.	Launch the image within VMware. 
    Install VMware and image from the following link - 
    https://www.mathworks.com/support/product/robotics/ros2-vm-installation-instructions-v2.html

2.	Copy the contents of racecar_src to catkin_ws/src

3.	Launch a terminal and run the following commands:
    •	sudo apt-get update
    •	gedit ~/.bashrc
    •	Include the following commands to the end of the file:
      o	source /opt/ros/melodic/setup.bash
      o	source /home/user/catkin_ws/devel/setup.bash

4.	Run the following commands to install required controllers:
    •	sudo apt install ros-melodic-velodyne  ros-melodic-ackermann-msgs  ros-melodic-joy ros-melodic-serial
    •	sudo apt install ros-melodic-controller-manager ros-melodic-controller-manager-msgs  ros-melodic-diff-drive-controller ros-melodic- forward-command-controller  ros-melodic-joint-state-controller 
    •	sudo apt install ros-melodic-position-controllers ros-melodic-controller-interface ros-melodic-gazebo-ros-control ros-melodic-control-msgs  ros-melodic-control-toolbox ros-melodic-combined-robot-hw ros-melodic-ros-control

5.	Route to catkin_ws and run the following command to install dependencies:
    •	rosdep install --from-paths src --ignore-src -r -y

6.	Run the following command to build your src files:
    •	catkin_make

7.	Run the following command to launch the gazebo world:
    •	roslaunch racecar_gazebo racecar.launch
