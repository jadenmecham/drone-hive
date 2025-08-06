# Realsense Camera Commands
- launch camera: ```roslaunch realsense2_camera rs_camera.launch```
- echo camera topic: ```rostopic echo /camera/color/image_raw```
- see camera live feed: ```rosrun image_view image_view image:=/camera/color/image_raw```
