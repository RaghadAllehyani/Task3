# Task3
Install and operate the arm package on the rose system:
open a new terminal, open a new workspace, and issue an empty first build command:
sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

Enter the arm package from the smart method account on GitHub by pasting it in the terminal:
git clone https://github.com/smart-methods/arduino_robot_arm.git 

Add dependencies: 
cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

write the following command to enter the (bashrc) file: 

sudo nano ~/.bashrc 

Update the (bashrc) file by adding a line at the end of the file:

source /home/r/catkin_ws/devel/setup.bash

then enter ctrl+O and Enter and then ctrl+X, and write the following command:

source ~/.bashrc

Copy the last command to turn on the arm:

roslaunch robot_arm_pkg check_motors.launch


![IMG_4062](https://user-images.githubusercontent.com/108802123/181349166-828d9162-279c-4941-ae6c-fb7676785657.jpg)



