cmake_minimum_required(VERSION 2.8.3)
project(laserscan_to_pointcloud)

find_package(catkin REQUIRED COMPONENTS
  laser_geometry
  roscpp
  sensor_msgs
  tf
)

catkin_package(
  CATKIN_DEPENDS laser_geometry roscpp sensor_msgs tf
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(laserscan_to_pointcloud src/laserscan_to_pointcloud.cpp)

target_link_libraries(laserscan_to_pointcloud
  ${catkin_LIBRARIES}
)
