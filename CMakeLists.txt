cmake_minimum_required(VERSION 2.8.3)
project(skeleton_follow)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)



## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs genmsg)

## Declare ROS messages and services
#add_message_files(FILES Num.msg)
#add_service_files(FILES AddTwoInts.srv)

## Generate added messages and services
generate_messages(DEPENDENCIES std_msgs)

## Declare a catkin package
catkin_package()


add_executable(skeleton_follow src/skeleton_follow.cpp)
target_link_libraries(skeleton_follow ${catkin_LIBRARIES})
include_directories(include ${catkin_INCLUDE_DIRS})




include_directories(/home/tt/astra_ws/src/skeleton_follow/include/)
include_directories(/home/tt/astra_ws/src/skeleton_follow/common/)





target_link_libraries(skeleton_follow /usr/lib/x86_64-linux-gnu/libsfml-graphics.so)
target_link_libraries(skeleton_follow /usr/lib/x86_64-linux-gnu/libsfml-system.so)
target_link_libraries(skeleton_follow /usr/lib/x86_64-linux-gnu/libsfml-window.so)
target_link_libraries(skeleton_follow /usr/lib/)

target_link_libraries(skeleton_follow /home/tt/astra_ws/src/skeleton_follow/lib/libastra.so -ldl -pthread)
target_link_libraries(skeleton_follow /home/tt/astra_ws/src/skeleton_follow/lib/libastra_core.so -ldl -pthread)
target_link_libraries(skeleton_follow /home/tt/astra_ws/src/skeleton_follow/lib/libastra_core_api.so -ldl -pthread)



