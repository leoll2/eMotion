cmake_minimum_required(VERSION 2.8.3)
project(scene_builder)

set(MSG_DEPS
  std_msgs
  geometry_msgs
  view_controller_msgs
)

find_package(catkin REQUIRED COMPONENTS genmsg message_generation rospy ${MSG_DEPS})

catkin_package(CATKIN_DEPENDS ${MSG_DEPS} message_runtime)

install(PROGRAMS
  src/eMotion_scene_builder
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
