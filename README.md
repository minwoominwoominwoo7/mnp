기본 Code는 AR marker 기반 Pick and Place 아래코드를 영상처리 기반으로 수정한 Code 임.   
현재 작업중인 GIT임 완성 Code 아님   
http://emanual.robotis.com/docs/en/platform/turtlebot3/manipulation/#pick-and-place   

# 설치 방법    
1. TB3 설치    
http://emanual.robotis.com/docs/en/platform/turtlebot3/pc_setup/#install-dependent-ros-packages     
2. open manipulator 설치    
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_setup/#install-ros-packages   
3. open manipulator with tb3 설치   
http://emanual.robotis.com/docs/en/platform/turtlebot3/manipulation/#software-setup   
4. darkent ros 설치    
git clone --recursive https://github.com/Affonso-Gui/darknet_ros.git    
5. D435 realsense 설치   
http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_applications/#installation-1   
6. jsk 설치     
```bash
$ sudo apt-get install ros-kinetic-jsk-recognition
$ sudo apt-get install ros-kinetic-jsk-topic-tools
$ sudo apt-get install ros-kinetic-libsiftfast
$ sudo apt-get install ros-kinetic-laser-assembler
$ sudo apt-get install ros-kinetic-octomap-server
$ sudo apt-get install ros-kinetic-nodelet
$ sudo apt-get install ros-kinetic-depth-image-proc
$ cd ~/catkin_ws/src/
$ git clone https://github.com/jsk-ros-pkg/jsk_common.git
$ catkin_ws && catkin_make
```
7. 변경된 code 설치    
mnp깃을 다운받아 src 폴더에 있는 파일들을 @ubuntu:~/catkin_ws/src$ 위치에 덮어씌우면 됨    
```bash
ubuntu:~$ git clone https://github.com/minwoominwoominwoo7/mnp.git
ubuntu:~$ cp -r ~/mnp/src/* ~/catkin_ws/src/
ubuntu:~$ catkin_ws && catkin_make
```

# 실행 명령어   
```bash
roslaunch open_manipulator_with_tb3_gazebo mnp_rooms.launch  
roslaunch open_manipulator_with_tb3_tools yolo_jsk_pose.launch  
roslaunch open_manipulator_with_tb3_tools rooms_mnp.launch use_platform:=false
roslaunch open_manipulator_with_tb3_tools task_controller_mnp.launch use_platform:=false
```

[![Video Label](http://img.youtube.com/vi/VflIXO7doro/0.jpg)](https://youtu.be/VflIXO7doro?t=0s)
