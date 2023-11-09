# ros2_control demo

##### 这是下面这个老哥的视频里的demo和完整实现
[bbot_demo](https://www.bilibili.com/video/BV1ku411G7UR/?spm_id_from=333.337.search-card.all.click)

## ！！准备事项！！
1. ros2 version foxy     
2. install ros2_control
3. install xacro (ros2 foxy默认不安装xacro)
4. 欢迎补充


## ！！getting started!!
1. 配置ros2_control的xacro文件
- 配置`hardware_interface`
  - `command_interface` `state_interface`
- 配置gazebo_ros2_control插件
  - 记得预留`controller_manager.yaml`的文件位置
2. 写controller_manager.yamal
3. 写launch文件
- 同时启动`rviz` `gazebo` `joint_state_publisher` `robot_state_publisher` `实例中的两个控制器`
  
4.！！启动！！
- `ros2 launch bbot_bringup bbot_bringup.launch.py`
- `ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_drive/cmd_vel_unstamped`  重定向控制小乌龟的键盘的那个话题



## 后记
1. 这和qiling学姐的区别是ros2_control的框架
2. 正在尝试用这种方式控制倒立摆平衡步兵
