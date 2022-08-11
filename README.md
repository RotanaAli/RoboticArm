# RoboticArm
Task 3 of Robotic and AI in Smart Methods Summer Training Program
-----------------------------------------------------------------
How to download and work on the Smart Method's Robotic Arm Joint Stick Package in ROS
-----------------------------------------------------------------
-Step # 1 : Download ROS, please follow the steps that i did before on this link:

https://github.com/RotanaAli/ROS

-Step # 2 : Open terminal in your Virtual Machine Box,
make and name a catkin workspace so we can make a package to work on the Robotic Arm,
by copying and pasting these commands:

[change 'noetic' in the following commands bellow if you are using something
other than it]

sudo apt-get install ros-noetic-catkin

[in this command bellow 'catkin_ws' is actually the name of the work space you
will create so you can change it to what you want to call it]

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

[To get access to Smart Methods Robotic Arm Packages]

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

[picture 1]

$ sudo apt-get install ros-noetic-moveit

$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

-Step # 3 : Add the workspace in the basharc file, copy and paste this coomand in the
terminal.

sudo nano ~/.bashrc

Copy and paste this folowing command on the last line of the terminal and make sure
the name you use is your own Virtual Machine name on this following command
[change 'me' to your account name and change 'catkin_ws' to your own
workspace file name]

source /home/me/catkin_ws/devel/setup.bash

Then,
 
ctrl + o

enter

ctrl + x 

-Step # 4 : Copy and past these commands to launch RVIZ program to work on
the Robotic Arm

source ~/.bashrc

roslaunch robot_pkg check_motors.launch

[picture 2]

RIVz download is complete and now you can customize the Robotic Arm to whatever you like, it's base_joint, elbow, shoulder, wrist and more.

-----------------------------------------------------------------
