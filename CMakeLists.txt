cmake_minimum_required(VERSION 3.0.2)
project(movement_api)

find_package(catkin REQUIRED COMPONENTS
  rospy
  geometry_msgs
  move_base_msgs
  actionlib
  tf
  message_generation
)

add_service_files(
  FILES
  GoToPose.srv
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS 
    rospy 
    geometry_msgs 
    move_base_msgs 
    actionlib 
    tf 
    message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
