cmake_minimum_required(VERSION 3.5)
set(PROJECT_NAME fast-guided-filter)
project(${PROJECT_NAME})
set(CMAKE_CXX_STANDARD 11)
FIND_PACKAGE(catkin_simple REQUIRED)
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
catkin_simple()

cs_add_library(${PROJECT_NAME} src/fastguidedfilter.cpp)
cs_install()
cs_export()
