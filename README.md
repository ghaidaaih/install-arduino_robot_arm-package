# install-arduino_robot_arm-package

1. creat catkin workspace
 ```sh
 cd ~
 mkdir catkin_ws/src -p
 cd ~/catkin_ws/
 catkin_make
   ```
2. install the arduino_robot_arm package
 ```sh
 cd ~/catkin_ws/src
 sudo apt install git 
 git clone https://github.com/smart-methods/arduino_robot_arm
   ```
3. install all the dependencies
 ```sh
 cd ~/catkin_ws
 rosdep install --from-paths src --ignore-src -r -y
 sudo apt-get install ros-noetic-moveit
 sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
 sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
 sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
 sudo nano ~/.bashrc
   ```
 at the end of the (bashrc) file 
 after the following 2 line
 <br>
  &nbsp;&nbsp;&nbsp;&nbsp; source /apt/ros/noetic/setup.bash
 <br>
  &nbsp;&nbsp;&nbsp;&nbsp; source /home/<your user name>/catkin_ws/devel/setup.bash

 <br>
 add the following line
 <br>
 
  ```sh
source /home/<your user name>/catkin_ws/devel/setup.bash
   ```
 <br>
 then tape in 
 <br> &nbsp;&nbsp;&nbsp;&nbsp; ctrl + o
 <br> &nbsp;&nbsp;&nbsp;&nbsp; Enter
 <br> &nbsp;&nbsp;&nbsp;&nbsp; ctrl + x
   
3. to Controlling the motors
 ```sh
 source ~/.bashrc
roslaunch robot_arm_pkg check_motors.launch
   ```
   
 **out put :**
 <br>
 ![out put](https://user-images.githubusercontent.com/109582339/181009715-5c348ff1-2007-4e16-a578-e21aa8952085.PNG) 
