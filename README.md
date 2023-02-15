

https://user-images.githubusercontent.com/80765148/219106097-d9e90557-1e36-406a-8a5d-6b7fb06fab36.mp4



🥀 [turtlebot3 with YOLOv3](https://docs.google.com/presentation/d/1JYjwY6ZqBugkgnGPtoBkekLW7GFiUyNSOJXIAy_f5Uo/edit?usp=sharing)  🥀

Metapackage for the turtlebot3 competition in the ROS system. The solution uses the YOLOv3 neural network. To run the metapackage, do the following:

1) run git clone from the [official github](https://emanual.robotis.com/docs/en/platform/turtlebot3/overview/) of the competition

git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020
git clone https://github.com/amburkoff/referee_console

2) run git clone of this package and install requirements

git clone https://gitlab.com/moksyasha/ros_moryachki.git

pip install -r requirements.txt

3) Execute the commands:

roslaunch turtlebot3_gazebo turtlebot3_autorace_2020.launch

roslaunch autorace_core_moryachki autorace_core.launch

rosrun referee_console mission_autorace_2020_referee.py

