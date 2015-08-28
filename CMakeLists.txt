cmake_minimum_required(VERSION 2.8.3)
project(iai_outdoor_models)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  roscpp
  tf 
  
  
)
catkin_package(
  DEPENDS 
    roscpp 
    gazebo_ros 
    tf
     
#  INCLUDE_DIRS 
#    include
)

include (FindPkgConfig)
if (PKG_CONFIG_FOUND)
  pkg_check_modules(GAZEBO gazebo)
endif()


include_directories(
  ${catkin_INCLUDE_DIRS}
  ${GAZEBO_INCLUDE_DIRS}
#  include
)

link_directories(${GAZEBO_LIBRARY_DIRS})
