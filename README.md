# AI-and-Robotics-ROS-Track-Task1
1- Download latest version of VirtualBox from this link: 
https://www.virtualbox.org/wiki/Downloads
2- Download Ubuntu 18.04 desktop image from this link:
https://releases.ubuntu.com/18.04/
3- Install VirtualBox on your pc
4- Create a new virtual machine using Ubuntu desktop image
5- Run the virtual machine, then install Ubuntu
6- Reboot the VM after installation completed, now Ubuntu is installed and ready to use
7- Install ROS using the following commands:
- sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu
-  $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-
-  latest.list'
- sudo apt install curl
- curl -s
- https://raw.githubusercontent.com/ros/rosdistro/master/ro
- s.asc | sudo apt-key add -
- sudo apt update
- sudo apt install ros-melodic-desktop-full
8- Environment setup using the following commands:
- echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
- source ~/.bashrc
9- Dependencies for building packages using the following commands:
- sudo apt install python-rosdep python-rosinstall python-
- rosinstall-generator python-wstool build-essential
- sudo apt install python-rosdep
- sudo rosdep init
- rosdep update
10-Test ROS after installation using the following command:
- roscore
11- Install catkin using the following command:
- sudo apt-get install cmake python-catkin-pkg python-
- empy python-nose python-setuptools libgtest-dev build-essential
12- Create and build a catkin workspace using the following commands:
- mkdir -p ~/catkin_ws/src
- cd ~/catkin_ws/
- catkin_make
- echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
13- Add the “arduino_robot_arm” package to “src” folder using the following commands:
- cd ~/catkin_ws/src
- sudo apt install git
- git clone https://github.com/smart-methods/arduino_robot_arm
 14- Install all the dependencies using the following commands:
- cd ~/catkin_ws
- rosdep install --from-paths src --ignore-src -r -y
- sudo apt-get install ros-melodic-moveit
- sudo apt-get install ros-melodic-joint-state-publisher ros-
  melodic-joint-state-publisher-gui
- sudo apt-get install ros-melodic-gazebo-ros-control joint-
  state-publisher
- sudo apt-get install ros-melodic-ros-controllers ros-
   melodic-ros-control
- catkin_make 
