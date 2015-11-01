cmake_minimum_required(VERSION 2.8.3)
project(ipab_lwr_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  sensor_msgs
  message_generation
)

add_message_files(
  FILES
  FriCommand.msg
  FriCommandJointPosition.msg
  FriCommandJointStiffness.msg
  FriCommandCartesianStiffness.msg
  FriCommandMode.msg
  FriState.msg
)

generate_messages(
  DEPENDENCIES
  sensor_msgs
  std_msgs
)

catkin_package(CATKIN_DEPENDS sensor_msgs std_msgs message_runtime)
