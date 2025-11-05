# Realsense Camera Commands
- launch camera: ```roslaunch realsense2_camera rs_camera.launch align_depth:=true depth_width:=640 depth_height:=480 depth_fps:=30 color_width:=640 color_height:=480 color_fps:=60```
- echo camera topic: ```rostopic echo /camera/color/image_raw```
- see camera live feed: ```rosrun image_view image_view image:=/camera/color/image_raw```
