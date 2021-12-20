in src..
sudo apt update
git clone https://github.com/ros/ros_tutorials.git -b galactic-devel
rosdep update
cd ..
rosdep install -i --from-path src --rosdistro galactic -y
colcon build

-- start new terminal
source /opt/ros/galactic/setup.bash
. install/local_setup.bash
ros2 run turtlesim turtlesim_node


-- https://industrial-training-master.readthedocs.io/en/melodic/_source/session7/ROS2-Basics.html
in src..
git clone -b galactic https://github.com/ros2/demos.git
git clone -b galactic https://github.com/ros2/examples.git
cd ..
rosdep update
rosdep install -i --from-path src --rosdistro galactic -y
colcon build
source /opt/ros/galactic/setup.bash
. install/local_setup.bash
ros2 launch dummy_robot_bringup dummy_robot_bringup.launch.py

-- 
rvis2
rqt