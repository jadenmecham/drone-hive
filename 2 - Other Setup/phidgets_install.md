## Install Phidgets Sensor Drivers
cd into src folder within catkin workspace folder. Do these steps:  
- `git clone -b noetic https://github.com/ros-drivers/phidgets_drivers.git`. Make sure to clone correct branch for ROS version!
- `rosdep install phidgets_drivers` or `sudo apt-get install libusb-1.0-0 libusb-1.0-0-dev`
- `git clone -b noetic https://github.com/ccny-ros-pkg/imu_tools.git`
- `cd ~/catkin_ws`
- `catkin build`
- `source devel/setup.bash`
  
Then to run one of the nodes:
- `roslaunch phidgets_accelerometer accelerometer.launch`
