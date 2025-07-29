## Install Phidgets Sensor Drivers
cd into src folder within catkin workspace folder. Do these steps:  
- `git clone -b noetic https://github.com/ros-drivers/phidgets_drivers.git`
- `rosdep install phidgets_drivers`
- `cd ~/catkin_ws`
- `catkin build`
  
Then to run one of the nodes:
- `roslaunch phidgets_accelerometer accelerometer.launch`
