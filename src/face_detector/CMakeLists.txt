cmake_minimum_required(VERSION 2.8.3)
project(face_detector)

find_package(catkin REQUIRED COMPONENTS
    rospy
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES face_detector
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

install(PROGRAMS
    src/face_detector
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
