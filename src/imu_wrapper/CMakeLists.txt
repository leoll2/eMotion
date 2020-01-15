cmake_minimum_required(VERSION 2.8.3)
project(imu_wrapper)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  geometry_msgs
  message_generation
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_service_files(
  FILES
  GetAcceleration.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS std_msgs message_runtime
)

install(PROGRAMS
  src/imu_serial
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
