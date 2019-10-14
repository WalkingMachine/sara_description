cmake_minimum_required(VERSION 2.8.3)
project(sara_description)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
        urdf
)

catkin_package(
)

###########
## Build ##
###########
include_directories(
  ${catkin_INCLUDE_DIRS}
)

link_directories(${GAZEBO_LIBRARY_DIRS})


find_package(roslaunch)

foreach(dir config launch meshes urdf)
    install(DIRECTORY ${dir}/
            DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)

# Gazebo is compiled with Protobuf 2.6.1 and Kortex with Protobuf 3.5.1
# The 2.6.1 includes are prepended to the include_directories so the Gazebo plugins we compile here build
include_directories(BEFORE ./include/)
link_directories(${GAZEBO_LIBRARY_DIRS})
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GAZEBO_CXX_FLAGS}")

install(DIRECTORY launch models worlds 
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
