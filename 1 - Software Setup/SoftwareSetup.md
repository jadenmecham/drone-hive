# Setup Offboard Computer
This is the setup for the computer that will control the drone. Your laptop is a good idea.
## Install Ubuntu
To setup your computer, you will first need to install the Ubuntu 20.04 operating system onto your computer. ***IMPORTANT:*** Do not install Ubuntu 24.04. It is only compatible with ROS2. We use ROS1, so we have to use Ubuntu 20.04. Follow these steps:
1. Download an image of Ubuntu 20.04 [here](https://releases.ubuntu.com/focal/)
2. Follow [these instructions](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview) to flash your computer with Ubuntu. Note that you will need a USB drive. You can either install Ubuntu alongside your current operating system or erase your current operating system. Either way works!
## Install ROS and Dependencies
This installs Robot Operating System (ROS) and all the required dependencies so we can run code on the drone later. 
1. Install git on the computer with ```sudo apt install git```
2. Clone [this repository](https://github.com/jadenmecham/hive_auto_install) to your computer with ```git clone https://github.com/jadenmecham/hive_auto_install```
3. Run the autoinstall script. ```cd /hive_auto_install```, then ```/.autoinstall.sh```
4. Answer Y to install ROS1 and N to install ROS2. Follow all other prompts as needed and then reboot at the end.
5. Once rebooted, run the catkin workspace builder script with ```cd /hive_auto_install```, then ```/.make_catkinws```. Answer Y to all prompts as needed and reboot at the end

***Tip:*** Sometimes a few of the packages will fail to build the first time around. Try building them individually with ```cd /catkin_ws```, then ```catkin build YOUR_PACKAGE```. For example: ```catkin build mavros```. Also make sure to source the catkin workspace after every build. The auto building script does this automatically but you will have to do it manually after building individual packages. Use ```source ~/catkin_ws/devel/setup.bash```. 

## Download QGroundControl
1. Navigate to [this link](https://docs.qgroundcontrol.com/master/en/qgc-user-guide/getting_started/download_and_install.html#old-stable-releases) to download the QGroundControl AppImage
2. Make the file executable with ```chmod +x ./QGroundControl.AppImage```
3. Run it with ```./QGroundControl.AppImage```

To make it easier to launch, you should add an alias to your bashrc file:
1. Open the file for editing with ```gedit ~/.bashrc```
2. At the end of the file, add something like ```alias QGC='./QGroundControl.AppImage'```
3. Save and close the file
4. Source the file with ```source ~/.bashrc```

 Now, you can type ```QGC``` into your terminal to launch QGroundControl.

# Setup the Drone's Onboard Computer 
Follow the same instructions as above to isntall Ubuntu, ROS1, and the required dependencies.


