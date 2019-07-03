## where_am_i ##
  This is a robot localization project. In this project, the ROS AMCL package is utilized to accurately localize a mobile robot inside a map in the Gazebo simulation environments.
### Configuration ###
- Ubuntu 16.04.6 xenial
- gazebo 7.15.0
- ROS kinetic kame
### Prerequisite package ###
  Some of the following package might need to be installed. You could install them as shown below:
```
  $ sudo apt-get install ros-kinetic-navigation
  $ sudo apt-get install ros-kinetic-map-server
  $ sudo apt-get install ros-kinetic-move-base
  $ sudo apt-get install ros-kinetic-amcl
```
### Installation ###
   First, create and initial a workspace:
```
  mkdir -p <YOUR_CURRENT_DIRECTORY>/catkin_ws/src
  cd catkin_ws/src
  catkin_init_workspace
```
  Second, clone the repository:
```
  git clone https://github.com/huanalexzhao/where_am_i.git
```
  The last, build the project:
```
  cd .. # go to the catkin_ws/ directory
  catkin_make
```
### Run the project ###
  Make sure you in the catkin_ws/ directory.
```
  source devel/setup.bash
  roslaunch my_robot world.launch
```
  Open a new terminal by ctr+shift+T.
```
  source devel/setup.bash
  roslaunch my_robot amcl.launch
```
  Open another terminal.
```
  source devel/setup.bash
  rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
