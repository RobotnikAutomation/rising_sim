cmake_minimum_required(VERSION 2.8.3)
project(rising_gazebo)

find_package(catkin REQUIRED COMPONENTS
    roscpp
    std_srvs
    std_msgs
    tf
    gazebo_ros
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(
  DIRECTORY launch worlds models rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
