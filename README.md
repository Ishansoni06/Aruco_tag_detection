# ARUCO TAG DETECTION

This repository will be about detecting and generating aruco tags in the gazebo ingintion . The aruco tag would be detected by the Husarion UGV (panther robot ).


# GENERATING ARUCO TAGS

![image](https://github.com/user-attachments/assets/0b9dbc97-5ad9-4dd5-b637-33b0a61a6b37)
![image](https://github.com/user-attachments/assets/87497733-edef-4111-8d07-6091adde9cf6)

to generate aruco tag in the world basically you need to add the image of the aruco tag and their model.config and model.sdf into a folder ( eg:- arucotag1 ) and then add that folder into /home/(your account name)/husarion_ws/src/husarion_gz_worlds/models . you can generate the aruco tags from https://chev.me/arucogen/ . 


# ARUCO DETECTION 

for aruco detection i have used the following github repositories :- 

1. https://github.com/JMU-ROBOTICS-VIVA/ros2_aruco
2. https://github.com/SaxionMechatronics/ros2-gazebo-aruco?tab=readme-ov-file ( this is based on the github repo mentioned above )

now while running the repositories we need to set the parameters in aruco_paramters.yaml according to the camera topics you are seeing in your ros2 topic list (in my case :- /front_cam/color/camera_info and /front_cam/color/raw_image ) 

after that run the aruco detection launch file , run the node . We would see two topics now /aruco_pose and /aruco_markers , echo those topics and run the panther robot using teleop key . when the robot camera detects the aruco tag it would return the pose of the bot , its ID and its orientation in space .

![image](https://github.com/user-attachments/assets/e3860558-8f3a-43b1-a1f7-67e9c44f9ed2)

[Screencast from 05-25-2025 09:46:46 PM.webm](https://github.com/user-attachments/assets/382de92a-0c68-4f8e-a591-c80b84af1ebc)
