# Manipulator 조작 메뉴얼
 Manipulator의 실제 하드웨어에서 조작

## Install ROS Kinetic package

> sudo apt-get update && sudo apt-get upgrade

> sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-gazebo* ros-kinetic-moveit* ros-kinetic-industrial-core

## 1. Joystick

5번 버튼 : home pose /
6번 버튼 : initial pose /
11번 버튼 : gripper close /
12번 버튼 : girpper open

주의 : 조작시 1번 버튼 누르면서 작동해야함!!

1. U2D2 권한 설정
> sudo chomd a+rw /dev/ttyUSB0

2. dynamixel controller 연결
> roslaunch open_manipulator_pro_controller open_manipulator_pro_controller.launch with_gripper:=true

3. joystick launch file 실행
> roslaunch open_manipulator_pro_teleop open_manipulator_pro_teleop_joystick.launch with_gripper:=true

![picture1](https://github.com/YDK18/OM_pro_joystick/image/picture1.png)


## 2. Moveit!

1. U2D2 권한 설정
> sudo chomd a+rw /dev/ttyUSB0

2. dynamixel controller 연결 및 Moveit! 실행
> roslaunch open_manipulator_pro_controller open_manipulator_pro_controller.launch with_gripper:=true use_moveit:=true

