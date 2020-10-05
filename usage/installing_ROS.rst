Setting Up ROS 
--------------------------

The following Documentation will allow you to have a better visualization process of Mapping your enviroment and Robot Navigation. 

Requirements: A modern Laptop with a display and UBUNTU 16.04 or more as its operating system. 

1. ROS stands for ROBOT OPERATING SYSTEM, and is a popular tool among customers using our robots.
2. Installing ROS is simple and you should be up running after following the below steps. (Mostly taken from ROS official Documentation)
3. Open your Terminal and Run This **sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'**
4. In the same terminal set up your keys by running this command **sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654**.
5. In the same terminal run **sudo apt update**.
6. Great! Congrats on reaching this step. Now as a final step you will be installing ROS. Run the following Command in the same terminal **sudo apt install ros-melodic-desktop-full**.
7. Once you have installed ROS, to make sure your system recognizes it all the time. Run the following two commands one at a time on the terminal **echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc** and **source ~/.bashrc**.
8. Finally to Check your ROS Version by typing **rosversion -d** if you have no errors in your installation. You should see your installed version on the screen.
