cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(iss3d)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (keypoints keypoints.cpp)
target_link_libraries (keypoints ${PCL_LIBRARIES})

add_executable (matching matching.cpp)
target_link_libraries (matching ${PCL_LIBRARIES})
