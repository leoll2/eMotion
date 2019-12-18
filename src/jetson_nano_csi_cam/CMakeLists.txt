cmake_minimum_required(VERSION 2.8.3)
project(jetson_nano_csi_cam)

find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  rospy
  sensor_msgs
  std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES jetson_nano_csi_cam
#  CATKIN_DEPENDS cv_bridge rospy sensor_msgs std_msgs
#  DEPENDS system_lib
)

install(PROGRAMS
    src/jetson_nano_cam
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
